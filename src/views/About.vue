<template>
  <div class="about">
    <h1>{{ product.name }}</h1>
    <p class="card-text">{{ product.subtitle }}</p>

    <div class="row">
      <div class="col-sm">
        <img src="@/assets/logo.png" style="padding: 10px;" class="card-img-top" alt="..."> 
      </div>
      <div class="col-sm">
        
        <div style="padding: 10px;">
          <h5 class="card-title">{{ product.price }} </h5>
          <div class="row">
            <div class="col-sm-3">
              <div class="form-group">
                <input type="text" class="form-control" value="1">
              </div>
            </div>
            <div class="col-sm">
              <a href="#" class="btn btn-block btn-success">Adicionar ao Carrinho</a>
            </div>
          </div>
        </div>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc orci massa, porta quis nunc nec, pharetra tempor eros. Morbi vehicula tellus a ligula malesuada pharetra. Pellentesque at consectetur ipsum, eu laoreet odio. Nam urna quam, convallis ut vehicula eget, scelerisque ut massa. Curabitur consectetur mauris ornare, fringilla sapien pretium, feugiat mauris.
        </p>
      </div>
    </div>    
  </div>
</template>

<script>
export default {
  data(){
    return {
      product : {}
    }
  },
  mounted() {
    const products = this.$store.state.products
    const product = products.find(product => product._id == this.$route.params.id)
    this.product = product
  }
}
</script>
