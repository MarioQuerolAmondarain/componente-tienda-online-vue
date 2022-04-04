<template>
  <div class="product-card">
      <img src="https://prod-mercadona.imgix.net/images/5e949a6f64b52be230b8f1084156dcd9.jpg?fit=crop&h=300&w=300" alt='a' />
      <br />
      <span>Pamerita</span>
      <br>

      <div id="añadirCarrito" v-if="contador == 0">
        <button color="primary" @click="contador++">
            Añadir al carro
        </button>
      </div>
      
      <div class="product-card-footer" id="enCarrito" v-if="contador > 0">
          <div class="product-card-footer-units">
              <small>En carro</small>
              <span><strong id='unit'>{{ contador }}</strong>/ud.</span>
          </div>
          <div>
              <button color="warn" @click="contador--">
                  <div>
                    -
                  </div>
              </button>
              <button color="accent"  @click="contador++">
                  +
              </button>
          </div>
      </div>
      </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => {
    return { contador: 0 };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
