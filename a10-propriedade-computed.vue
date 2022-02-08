<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<div id="app">
    <P>Computed: {{computed_contadores}}</P> <!-- imprime o retorno da função computed_contadores definida em
                                            computed:. A programação dessa função contém as variaveis
                                            numCliques e contador, quando essas variáveis sofrem alteração
                                            indiretamente a função computed_contadores é executada, mas somente
                                            se houver alteração nos valores dessas variáveis. Quem está programada
                                            para alterar os valores dessas duas variáveis numCliques e contador
                                            são as funções SomaClique e SomaContador(o contador só aceita somar quando numCliques é um
                                            número par) se não haver alteração de valores de uma dessas variáveis não haverá acionamento
                                            da função computed_contadores.
                                            -->
    <P>Contador: {{contador}}</P>
    <p>Cliques: {{numCliques}}</p>
    <p>CliqueTeste: {{cliqueTeste}}</p>

    <button v-on:click="SomaClique">Soma Clique</button> <!-- um evento click faz executar a função SomaClique-->
    <button v-on:click="SomaContador">Soma Contador</button> <!-- um evento click faz executar a função SomaContador-->
    <button v-on:click="Teste">Teste click sem computar dados</button> <!-- um evento click faz executar a função Teste
                                                                            como essa função é não funcionalidade relacionada
                                                                            às variaveis numCliques e contador, a função
                                                                            computed_contadores não é acionada.-->
    
    
</div>

<script>
    new Vue (
        {
            el: '#app',
            data: {
                numCliques: 0,
                contador:0,
                computed:0,
                cliqueTeste:0

            },
            methods: {
                SomaClique() {
                    this.numCliques++
                },
                SomaContador() {
                	par = this.numCliques % 2
                    if(par==0) {this.contador++}
                },
                Teste() {
                		this.cliqueTeste++
                }

            },
            filters: {

            },
            computed: {
            	computed_contadores() {
              	c = this.contador
                q = this.numCliques
                return this.computed++
              }

            }
        }
    )
</script>