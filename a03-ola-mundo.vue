<script src=<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>></script>

<div id='app'>  <!-- tag de identificação para o Vue -->
  <h3>
    {{titulo}} <!-- renderiza a variavel definida no Vue -->
  </h3>
  <p>
    {{paragrafo}} <!-- renderiza a variavel definida no Vue -->
  </p>
  <button v-on:click="alterarTitulo"> <!-- esuta um evento click-->
    Pressione e Veja
  </button>
</div>

<script>
  new Vue( 
    {
      el: '#app',
      data: {
        titulo: 'Minha aplicação em Vue',
        paragrafo: 'olá mundo'
      },
      methods: {
        alterarTitulo: function() {
          this.titulo = 'Primeira aplicação em Vue'
        }
      }
    }
  )
</script>