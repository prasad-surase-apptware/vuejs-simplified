<script setup>
import CSSModules from "./components/CSSModules.vue";
import DataBinding from "./components/DataBinding.vue";
import EventHandling from "./components/EventHandling.vue";
import StylingComps from "./components/StylingComps.vue";
import VueReactivity from "./components/reactivity/VueReactivity.vue";
import FormHandling from "./components/FormHandling.vue";
import ComputedProperty from "./components/ComputedProperty.vue";
import VueDirectives from "./components/VueDirectives.vue";
import VueProps from "./components/VueProps.vue";
import ProductsPage from "./pages/ProductsPage.vue";
import CustomButton from "./components/CustomButton.vue";
import CustomWrapper from "./components/CustomWrapper.vue";
import A from "./components/ProvideInject/A.vue";
import LifecycleHooks from "./components/LifecycleHooks.vue";
import VueComposables from "./components/VueComposables.vue";
import CustomDirectives from "./components/CustomDirectives.vue";
import DataFetching from "./components/DataFetching.vue";

const userEmail = "prasad.surase@apptware.com";
</script>

<template>
  <!-- <StylingComps />
  <hr />
  <CSSModules />
  <hr /> -->
  <!-- <DataBinding /> -->
  <!-- <hr /> -->
  <!-- <EventHandling /> -->
  <!-- <VueReactivity /> -->
  <!-- <FormHandling /> -->
  <!-- <ComputedProperty /> -->
  <!-- <VueDirectives /> -->
  <!-- <VueProps userName="Prasad" :email="userEmail" /> -->
  <!-- <ProductsPage /> -->

  <!-- <CustomButton>
    form
  </CustomButton> -->

  <!-- <CustomButton>
    <h4>Buy Now</h4>
  </CustomButton>
  <CustomButton>Register!</CustomButton>

  <CustomButton />

  <hr />

  <CustomWrapper>
    <template v-slot:one>
      <h1>This is for slot 1</h1>
    </template>

    <template #two>
      <h1>This is for slot 2</h1>
    </template>
  </CustomWrapper> -->

  <hr />

  <!-- Provide & inject -->
  <!-- <A /> -->

  <!-- <LifecycleHooks /> -->

  <!-- <VueComposables /> -->

  <!-- <CustomDirectives /> -->

  <DataFetching />
</template>

<style></style>
