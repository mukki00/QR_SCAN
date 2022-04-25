<template>
  <h1>Bill Table</h1>
  <p>{{ totalamount }}</p>
  <p>{{ colamountheader }}</p>
  <p>{{ statusinfo }}</p>
</template>
<script>
export default {
  name: "BillTable",
  props: {
    totalamount: String,
    colamountheader: String,
    statusinfo: String,
  },
};
</script>
<style></style>
