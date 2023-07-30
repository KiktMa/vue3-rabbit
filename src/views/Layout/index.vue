<script setup>
import LayoutNav from "./components/LayoutNav.vue";
import LayoutHeader from "./components/LayoutHeader.vue";
import LayoutFooter from "./components/LayoutFooter.vue";
import LayoutStickyVue from "./components/LayoutSticky.vue";

import { useCategoryStore } from "@/stores/category";
import { onMounted } from "vue";

const categoryInst = useCategoryStore()

onMounted(()=>categoryInst.getCategoryList())
</script>

<template>
  <LayoutNav />
  <LayoutStickyVue />
  <LayoutHeader />
  <RouterView />
  <LayoutFooter />
</template>