<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<div id="app">
    <p>
     Debug para ver a captura de novoNome:{{novoNome}}
    </p>
    <input type="text" v-model="novoNome"> <!-- entrada para a digitação e captura dos valores digitados na
                                                    variável novoNome definida em data:-->
    <button v-on:click="Add">+1 nome</button> <!--Captura a ocorrencia de um click chamando a 
                                                    função Add definida em methods:-->
    <ul>
      <li v-for="nome in nomes">{{nome | CaixaAlta}}</li> <!-- v-for Laço que percorre todo o array nomes[], definido 
                                                                em data:, sendo atribuido cada ocorrência à variavel
                                                                'nome' cada elemento do array e renderizando 
                                                                dinamicamente cada linha-->
                                                          <!-- o sinal PIPE, redireciona a saída para o Filter: de
                                                                nome CaixaAlta() onde a variável 'nome' é passada
                                                                como um parâmetro para essa função que retornará o
                                                                valor tratado que será renderiazado no v-for-->
    </ul>
    

</div>

<script>
    new Vue (
        {
            el: '#app',
            data: {
                nomes: [], // cria a variável nomes como um array
                novoNome: '',
            },
            methods: {
                Add: function() {
                    this.nomes.push(this.novoNome), //push é um comando de atribuição de valores em array
                    this.novoNome = ''
                }
            },
            filters: {
              CaixaAlta: function(parm1) {
					return parm1.toUpperCase() /* como resultado do tratamento do filtro, a variável parm1
                                                    é retornada com o tratamento da função toUpperCase()
                                                */
              }
            }
        }
    )
</script>