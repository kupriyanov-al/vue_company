<script setup>

import LayoutMain from './Layouts/LayoutMain.vue';
import { ref, onMounted } from "vue";
import axios from 'axios';


const products = ref([]);
const category = ref([]);


const fetchProduct = async() =>{
  try {
    fetchCategory()
    const {data} =await axios.get('https://bb2763669061f9ac.mokky.dev/items')
    //products.value=data
    // this.posts = this.posts.map(p => {
    //     p.author = users.find(u => u.id === p.userId)
    
    products.value =data.map(p=> {
       
        p.category = category.value.find(cat=>cat.id===p.idCategory)['category']

        console.log(p.category)
        return p
    }
          
  )  
}
catch (error) {
     console.log(error)
  }
}  

const fetchCategory = async() =>{
  try {
    const {data} =await axios.get('https://bb2763669061f9ac.mokky.dev/category')

    category.value=data
  } catch (error) {
     console.log(error)
  }
}

// const category = 

onMounted(()=>{
    fetchProduct(),
    fetchCategory()
   
})

// export const getRecipeById = async(id) =>{
//     const {data} =await axios.get( `${URL_RECEPE_BY_ID}${id}`)
//    return data[0]; //возвращаем 1 строку
// }

</script>

<template>
    <LayoutMain>
        <template #title>
            Products 
        </template>
        <template #inner>
            <el-row>
                <el-col v-for="(product, index) in products" :key="product.id" :span="4" >
                    <el-card  class="card">
                        <!-- <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"
                            class="image" /> -->
                        <div style="padding: 14px">
                            <span>{{ product.productName }}</span>
                            <div class="bottom">
                                <div class="time">{{product.idCategory}}</div>
                                <div class="time">{{product.category}}</div>
                                <el-button text class="button">Operating</el-button>
                            </div>
                        </div>
                    </el-card>
                </el-col>
            </el-row>
        </template>

    </LayoutMain>
</template>

<style scoped lang="scss">
@import '@/assets/main.scss';

.time {
    font-size: 12px;
    color: #999;
}

.bottom {
    margin-top: 13px;
    line-height: 12px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.button {
    padding: 0;
    min-height: auto;
}

.image {
    width: 100%;
    display: block;
}

.el-col {
    // display: flex;
    // margin: -15px; 
//    margin: 10px 25px 10px 0;
    //gap: 3px;
}

.card {

    
    margin: 10px 25px 10px 0;
}

</style>