<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h1 class="page-title">Welcome to Ecom</h1>
        </div>
        <div v-for="item in items" class="col-lg-4">
          <div
            class="card mb-2"
            style="width: 18rem; height: 18rem"
          >
            <img src="images/products.jpg" class="card-img-top" alt="..." />
            <div class="card-body">
              <h5 class="card-title">Name : {{ item.name }}</h5>
              <p class="card-text">Price : {{ item.price }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
  layout: "dashboard",
  data() {
    return {
      items: [],
    };
  },
  methods: {
    getItems() {
      this.$axios.get("http://ecom.products/api/products").then((res) => {
        this.items = res.data.items;
        // console.log(this.items);
      });
    },
  },
  mounted() {
    this.getItems();
  },
};
</script>
<style>
.page-title {
  padding: 15px;
  color: rgb(42, 5, 78);
  font-size: 4rem;
}
</style>
