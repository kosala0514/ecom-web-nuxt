<template>
  <div>
    <div class="container">
        <div class="row">
            <div class="col-lg-12 text-center">
                <h1 class="page-title mt-5">Products</h1>
                <hr  />
            </div>
            <div v-for="item in items" class="col-lg-4">
            <div class="card" style="width: 18rem;">
              <img src="images/products.jpg" class="card-img-top" alt="...">
              <div class="card-body">
                <h5 class="card-title">{{ item.name }}</h5>
                <p class="card-text">Rs:{{ item.price }}.00</p>
                <div>
                  <a v-if="item.status ==0" class="btn btn-danger" href="#">Inactive</a>
                  <a v-else class="btn btn-success" href="#">Active</a>
                </div>
              </div>
            </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  layout: 'dashboard',
  data(){
    return {
      items:[],
    }
  },
  methods:{
    getItems(){
      this.$axios.get('http://ecom.products/api/products').then(res =>{
        this.items = res.data;
      });
    },
  },
  mounted() {
    this.getItems();
  },
}
</script>
