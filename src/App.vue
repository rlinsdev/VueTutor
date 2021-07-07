<template>
  <h1>{{ title }}</h1>
    <div v-if="showModal">  
      <Modal theme="sale" @close="toggleModal" >
        <template v-slot:links>
          <a href="#">sign up now</a>
          <a href="#">more info</a>
        </template>
        <h1>Ninja Givaway</h1>
        <p>Grab your ninja</p>
      </Modal>
    </div>
  <button @click.alt="toggleModal">Open Modal (Alt)</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data(){ 
    return {
      title: "My First Vue App",
      header: "Sign up for the Giveaway!",
      text:"Grab your ninja swag or half price!",
      showModal: false
    }
  },
  methods : {
    toggleModal() {
      this.showModal = !this.showModal;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.modal h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
.modal p {
  font-style: normal;
}

.modal.sale {
  background: crimson;
  color: white;
}
.modal.sale h1 {
  color: white;
}
</style>
