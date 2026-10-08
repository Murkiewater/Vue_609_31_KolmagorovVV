<script setup>
<<<<<<< HEAD
import { onMounted, ref } from 'vue'
import axios from 'axios'

import ProductList from './components/ProductList.vue';
const items = ref([]);
const fetchItems = async () => {
  try {
    const { data } = await axios.get(
      'https://5da094f59ee2cbee.mokky.dev/items'
    );
    items.value = data.map((object) => ({
      ...object,
      isFavorite: false,
      isAdded: false,
    }));
  } catch(error) {
    console.log(error);
  }
};
onMounted(async () => {
  await fetchItems();
});
</script>

<template>
  <body class="flex flex-col justify-between h-dvh">

    <div class="mb-25">
      <nav class="border-b border-b-slate-200">
        <div class="mx-auto w-[1440px] py-3">
          <div class="flex items-center justify-between">
            <div class="flex items-center gap-3">
              <img  
                src="/logo.svg" 
                alt="logo"
              >
              <p class="text-sm">
                Лучшие цены <br />
                в интернет магазинах
              </p>
            </div>
            <ul class="flex gap-7">
              <li>
                <a 
                  href=""
                  class="flex gap-3 items-center"
                >
                  <span
                    class="p-3.5 rounded-xl bg-slate-100 hover:bg-slate-200 transition"
                  >
                    <img 
                      src="/cart-icon.svg" 
                      alt=""
                    >
                  </span>
                  Корзина
                </a>
              </li>
              <li>
                <a 
                  href=""
                  class="flex gap-3 items-center"
                >
                  <span
                    class="p-3.5 rounded-xl bg-slate-100 hover:bg-slate-200 transition"
                  >
                    <img 
                      src="/like-outline.svg" 
                      alt=""
                    >
                  </span>
                  Избранное
                </a>
              </li>
              <li>
                <a 
                  href=""
                  class="flex gap-3 items-center"
                >
                  <span
                    class="p-3.5 rounded-xl bg-slate-100 hover:bg-slate-200 transition"
                  >
                    <img 
                      src="/orders-icon.svg" 
                      alt=""
                    >
                  </span>
                  Заказы
                </a>
              </li>
            </ul>
            </div>
        </div>
      </nav>
      <main class="mx-auto w-[1440px] pt-10">
        <h1 class="text-[40px] font-bold mb-5">Каталог</h1>
        <product-list :items="items"></product-list>
      </main>
    </div>
    <footer class="p-6 bg-slate-100">
      <div class="text-center text-slate-500">
        Copyright © 2023 Behoof, Inc. Все права защищены
      </div>
    </footer>
  </body>

=======
import MyComponent from './components/MyComponent.vue';
import MyNewComponent from './components/MyNewComponent.vue';
</script>

<template>
  <MyComponent />
  <MyNewComponent />
>>>>>>> 4880e880e70ec34103746661e86dfeafa4cfce13
</template>

<style scoped></style>
