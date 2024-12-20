<script setup>
import { RouterLink, RouterView } from 'vue-router'
//import HelloWorld from './components/HelloWorld.vue'
import Menubar from 'primevue/menubar';
</script>

<template>
  <div class="container mt5 left">
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/HexConverter">HexConverter</RouterLink>
      </nav>
    </div>
  </div>

  <RouterView />
</template>


<script>
import { ref } from "vue";
import { useRouter } from 'vue-router';

const router = useRouter();

const items = ref([
  {
    label: 'Home',
    icon: '',
    command: () => {
      router.push('/src/App.vue');
    }
  },
  {
    label: 'Hex Converter',
    icon: '',
    command: () => {
      router.push('/src/views/HexConverter.vue');
    }
  },
  {
    label: 'External',
    icon: 'pi pi-home',
    command: () => {
      router.push('/src/views/AboutView.vue');
    }
  }
]);
</script>