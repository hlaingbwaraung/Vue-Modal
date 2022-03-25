<template>
  <h1>hi </h1>
  <div v-if="showModal">
      <Modal :theme="theme1" @close="showModal=false">
        <h2>Success log in</h2>
        <p>welcome user</p>
        </Modal>
  </div>
   <div v-if="dangerModal">
      <Modal :theme="theme2" @close="dangerModal=false">
        <h2>Are u sure to delete</h2>
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
       theme1:"success",
       theme2:"danger",
       showModal:false,
       dangerModal:false,    
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

