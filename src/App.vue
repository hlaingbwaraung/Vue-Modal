<template>
  <h1>hi </h1>
  <div v-if="showModal">
      <Modal :theme="theme" @close="showModal=false">
        <h1>Success log in</h1>
        <p>welcome user</p>
        </Modal>
  </div>
   <div v-if="dangerModal">
      <Modal :theme="theme" @close="dangerModal=false">
        <h1>Are u sure to delete</h1>
        <p>Its hard to say goodbye</p>
        </Modal>
  </div>
  <button @click="showModal=true">open modal</button>
  <button @click="dangerModal=true">Delete modal</button>

</template>

<script>
import Modal from "./components/Modal.vue"
export default {
  data(){
    return{   
       theme:"danger",
       showModal:false,    
    }
  },
  components:{
    Modal
  }
}
</script>

<style scoped>
 h1{
  color: aqua;
}
</style>

