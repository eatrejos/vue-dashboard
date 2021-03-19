<template>
  <div class="border md:m-2 lg:m-5 shadow-md  rounded-md">
    <div class="p-8 flex justify-between " >
      <div>
        <div class="card-title">
          <p>
            {{name}}
            <small :class="[{'bg-green-200':status == 1},{'bg-red-200':status == 2}, 'text-sm px-3 py-1 rounded-full']">
              {{status_text}}
            </small>
          </p>
        </div>
        <div class="card-text mt-2 ">{{text}}</div>
      </div>
      <div class="w-12 h-12">
        <img :src="getImage(avatar)" :alt="name" class=" rounded-full">
      </div>      
    </div>
    <div class="flex border-t">
      <div class="p-5 w-1/2 flex border-r h-30 justify-center">
        <div class=" mr-3">
          <svg width="20" height="20" viewBox="0 0 17 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0.253 1.884L8.25 5.882L16.247 1.884C16.2174 1.37444 15.9941 0.895488 15.6228 0.545227C15.2516 0.194965 14.7604 -9.35847e-05 14.25 3.36834e-08H2.25C1.73958 -9.35847e-05 1.24845 0.194965 0.877178 0.545227C0.505908 0.895488 0.282604 1.37444 0.253 1.884Z" fill="#9CA3AF"/>
            <path d="M16.25 4.118L8.25 8.118L0.25 4.118V10C0.25 10.5304 0.460714 11.0391 0.835786 11.4142C1.21086 11.7893 1.71957 12 2.25 12H14.25C14.7804 12 15.2891 11.7893 15.6642 11.4142C16.0393 11.0391 16.25 10.5304 16.25 10V4.118Z" fill="#9CA3AF"/>
          </svg>        
        </div>
        <div class="p-title">Email</div>
      </div>
      <div class="p-5 w-1/2 flex h-30 justify-center">
        <div class="mr-3 ">
          <svg width="20" height="20" viewBox="0 0 17 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0.75 1C0.75 0.447715 1.19772 0 1.75 0H3.90287C4.39171 0 4.8089 0.353413 4.88927 0.835601L5.62858 5.27147C5.70075 5.70451 5.48206 6.13397 5.0894 6.3303L3.54126 7.10437C4.65756 9.87832 6.87168 12.0924 9.64563 13.2087L10.4197 11.6606C10.616 11.2679 11.0455 11.0492 11.4785 11.1214L15.9144 11.8607C16.3966 11.9411 16.75 12.3583 16.75 12.8471V15C16.75 15.5523 16.3023 16 15.75 16H13.75C6.5703 16 0.75 10.1797 0.75 3V1Z" fill="#9CA3AF"/>
          </svg>
      
        </div>
        <div class="p-title">Call</div>
      </div>
    </div>
    
  </div>
</template>
<script>


export default {
    name: 'Card',
    props:{
      status:{type:Number, default :0},
      status_text:{type:String, default :''},
      name:{type:String, default :''},
      text:{type:String, default :''},
      avatar:{type:String, default :''},
    },
    data() {
     return{}
    },
    methods: {
      getImage: function (el) {
        return require(`@/assets/${el}.jpg`);
      }
    }
}
</script>
<style scoped>
.card-title{
font-family: sans-serif;
font-style: normal;
font-weight: 500;
font-size: 20px;
line-height: 22px;
}
.card-text{
  font-family: sans-serif;
font-style: normal;
font-weight: 400;
font-size: 20x;
line-height: 20px;
color: #6B7280;
}
</style>



