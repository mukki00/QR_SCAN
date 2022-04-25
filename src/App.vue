<script>
import PaymentStatus from "./components/PaymentStatus.vue";

export default {
  name: "App",
  components: { PaymentStatus },
  data() {
    return {
      status: "STATUS",
      statusHead: "STATUS_HEAD",
      statusText: "STATUS_TEXT",
      statusTotal: "STATUS_TOTAL",
      totalAmountPaidUnPaid: "TOTAL AMOUNT PAID UNPAID",
      colAmountHead: "COL AMOUNT HEAD",
      message: {
        bill: {
          to: "TO",
          trandate: "TRANDATE",
        },
        LKR: "LKR",
      },
      billPay: {
        company: "COMPANY",
      },
      statusPay: "STATUS_PAY",
      locale: {
        currency: "LKR",
        payDate: "234234",
      },
    };
  },
  methods: {
    created() {
      console.log("message " + this.message);
    },
  },
};
</script>
<template>
  <PaymentStatus
    :status="status"
    :statusHead="statusHead"
    :billPay="billPay"
    :message="message"
    :statusPay="statusPay"
    :statusTotal="statusTotal"
    :locale="locale"
    :statusText="statusText"
    :totalAmountPaidUnPaid="totalAmountPaidUnPaid"
    :colAmountHead="colAmountHead"
  />
</template>
<style>
@import "./assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
