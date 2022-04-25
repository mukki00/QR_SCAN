<template>
  <h1>{{ status || statusHead }}</h1>
  <div>
    <p>
      <span>{{ message.bill.to }}</span>
      <span>{{ billPay.company }}</span>
    </p>
    <p>
      <span>{{ status || statusPay }}</span>
      <span>{{ message[locale.currency] }}</span>
    </p>
    <p>
      <span>{{ message.bill.trandate }}</span>
      <span>{{ locale.payDate }}</span>
    </p>
  </div>
  <div>
    <p :class="[status ? 'error_msg' : '', 'info']">
      {{ status || statusText }}
    </p>
  </div>
  <BillTable
    :totalamount="totalAmountPaidUnPaid"
    :colamountheader="colAmountHead"
    :statusinfo="status || statusTotal"
  />
</template>
<script>
import BillTable from "./BillTable.vue";
export default {
  name: "PaymentStatus",
  props: {
    status: String,
    statusHead: String,
    billPay: Object,
    message: Object,
    statusPay: String,
    locale: Object,
    statusText: String,
    totalAmountPaidUnPaid: String,
    colAmountHead: String,
    statusTotal: String,
  },
  components: { BillTable },
};
</script>
<style scoped>
.error_msg {
  color: red;
}
.info {
  padding: 10px 0px 5px 0px;
}
</style>
