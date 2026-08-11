<script setup lang="ts">
import { renderShopPayButton, type ShopPayButtonOptions } from "@shopify/hydrogen";
import { computed } from "vue";

const props = defineProps<{
  variants?: ShopPayButtonOptions["variants"];
  checkoutUrl?: string;
  paymentOption?: ShopPayButtonOptions["paymentOption"];
  source?: string;
  sourceToken?: string;
  disabled?: boolean;
  width?: string;
  borderRadius?: string;
  accessibilityLabel?: string;
}>();

const html = computed(() => renderShopPayButton(props));
</script>

<template>
  <!-- Trusted markup produced by @shopify/hydrogen; user inputs are escaped by renderShopPayButton. -->
  <div style="display: contents" v-html="html" />
</template>
