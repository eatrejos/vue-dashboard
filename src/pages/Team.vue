<template>
   <div>
     <div>
      <div class="p-title mx-4">
        Pinned Contacts
      </div>
      <div class="w-full sx:w-1/1 sm:w-1/1 md:w-1/2 lg:w-1/3 mb-base inline-block" v-for="card in cards" :key="card.$index">
        <Card :status="card.status" :status_text="card.status_text" :name="card.name" :text="card.text" :avatar="card.avatar"/>         
      </div>              
    </div>
    <div>
      <div class="p-title m-4">
        Pinned Contacts
      </div>
      <div class="w-full">
        <ContactsTable :contacts="cards" />
      </div>
      
    </div>
      
   </div>
</template>

<script>
import Card from '../components/Card'
import ContactsTable from '../components/Table'
import cards from '../json/cards.json'
export default {
    name: 'Team',
    components:{
      Card,
      ContactsTable
    },
    data() {
      console.log('cards',cards)
     return{
       
       cards:cards
     }
    },    
    mounted () {
        
    }
}
</script>
<style scoped>
.p-title{
font-family: sans-serif;
font-style: normal;
font-weight: 500;
font-size: 20px;
line-height: 22px;
}
</style>
