<template>
     <div class="card" style="width: 18rem;">
        <div class="card-header">
            <h5 class="card-title">{{ product.name }}</h5>
        </div>                  
        <div class="card-body">
        <img src="@/assets/logo.png">
        <p class="card-text">{{ product.price }}</p>
        <p class="card-text">{{ product.subtitle }}</p>
        <a href="#" class="btn" :class="{'btn-outline-success': !product.active, 'btn-success': product.active}">Comprar</a>
        </div>
        <div class="card-footer">
            <router-link style="display: block;margin-top: 10px;color:#333;" :to="`/about/${product._id}`">Mais Detalhes</router-link> 
        </div>
    </div>
</template>

<script>
export default {
    props: {
        product: {
            type: Object,
            required: true
        }
    }
}
</script>