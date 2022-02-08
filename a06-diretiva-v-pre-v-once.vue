<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14"></script>

<div id="app"> <!-- tag para o Vue-->
  <p v-pre>{{nome}}</p> <!-- // não executa as instruções HTML da linha, mostrando o código ajuda a depurar-->
  <p v-once>{{nome}}</p> <!-- // Renderiza/imprime uma única vez, mesmo que seja
                           redefinindo a variável 'nome', essa linha não rederizará mais. Feito no botão click. -->
  <p v-text="nome"></p> <!-- Rederiza/imprime a variavel como texto-->
  <button v-on:click="mn1">Muda Nome</button> <!-- escuta evento click e aciona a função mn1 -->

</div>

<script>
    new Vue(
        {
            el: '#app',
            data: {
							nome: 'Macelo',
            },
            methods: {
            	mn1: function() {
              	this.nome = 'Marcelo Vasconcellos'
              }  
            }
        }
    )
</script>