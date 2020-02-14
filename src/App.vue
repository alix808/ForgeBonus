<template>
  <div id="app">
    <NavBar />
    <div class="container">
      <AddTodo />
      <Todos :info="infoOne" />
      <Todos :info="infoTwo" />
      <Todos :info="infoThree" />
    </div>
    <Modal />
  </div>
</template>

<script>
import Todos from './components/Todos.vue';
import AddTodo from './components/AddTodo.vue';
import Modal from './components/Modal.vue';
import NavBar from './components/NavBar.vue';

export default {
  name: 'App',
  components: {
    Todos,
    AddTodo,
    Modal,
    NavBar
  },
  data: () => ({
    infoOne: {
      type: 'lifeChanging',
      title: 'Life Changing',
      background: 'linear-gradient(180deg, #05f, #09f)'
    },
    infoTwo: {
      type: 'important',
      title: 'Important',
      background: 'linear-gradient(180deg, #91f, #70f)'
    },
    infoThree: {
      type: 'meh',
      title: 'Meh',
      background: 'linear-gradient(180deg, #f08, #d0e)'
    }
  })
};
</script>

<style>
@font-face {
  font-family: 'AktivGrotesk_Trial_Bd';
  src: url('./TrialStaticFonts/AktivGrotesk_Trial_Bd.ttf') format('opentype');
}

body {
  font-family: 'AktivGrotesk_Trial_Bd';
  line-height: 1.6;
  background: rgba(10, 10, 10, 1);
}
.container {
  max-width: 1100px;
  margin: auto;
  overflow: auto;
  padding: 0 2rem;
}
</style>
