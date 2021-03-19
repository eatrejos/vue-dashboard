<template>
  <div class="">
    <table class=" border shadow-md rounded-lg w-full bg-white">
      <thead>
        <tr class="border-b bg-gray-100">
          <td class="p-3 text-left text-gray-400">NAME</td>
          <td class="p-3 text-left text-gray-400">TITLE</td>
          <td class="p-3 text-left text-gray-400">STATUS</td>
        </tr>
      </thead>
      <tbody v-if="contacts">
        <tr v-for="item in contacts" :key="item.$index" class="border">
          <td class="p-6">
            <div class="flex">
              <div class="w-12 h-12">
                <img :src="getImage(item.avatar)" :alt="item.name" class="rounded-full">
              </div>            
              <div class="ml-4">
                <p>{{item.name}}</p>
                <p class="text-gray-400">{{item.email}}</p>
              </div>
            </div>
          </td>
          <td class=" p-4">
            <p>
              {{item.text}}
            </p>
            <p class="text-gray-400">
              {{item.text}}
            </p>
          </td>
          <td class=" p-4">
            <span :class="[{'bg-green-200':item.status == 1},{'bg-red-200':item.status == 2}, 'px-3 py-1 rounded-full']">
              {{item.status_text}}
            </span>            
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>


<script>
export default {
  name:"ContactsTable",
  props:{
    contacts:{type:Array, default:null}
  },
  data() {
    return {}
  },
  methods:{
    getImage: function (el) {
          return require(`@/assets/${el}.jpg`);
    }
  }
}
</script>

<style>

</style>