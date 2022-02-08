<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<div id="app">
    <p>Digite sua mensagem</p>
    <input type="text" v-model="watch_mensagem"> <!-- v-model alimenta as variáveis declarada em data: em real-time, já sabemos
                                                    a variável 'watch_mensagem' foi definida em data: e com o
                                                    mesmo nome 'watch_mensagem' uma função foi definida em watch:.
                                                    E na propriedade watch: é possível incluir monitoramento e
                                                    tratamento caracter a caracter digitado. Nesse exemplo será
                                                    monitorado o tempo decorrente entre caracteres, se for inferior
                                                    a 2 segundo (2000 milisegundos) a variável 'digitando' é true
                                                    se o tempo entre a digitação for superior a 2 seguntos o valor
                                                    da variável 'digitando' passa a ser false-->
                                                    
    <p v-if="digitando">Digitando ...</p>
</div>

<script>
    new Vue (
        {
            el: '#app',
            data: {
                digitando: false,
                watch_mensagem: ''
            },
            methods: {

            },
            filters: {

            },
            computed: {

            },
            watch: {
                watch_mensagem(novoValor, antigoValor) {
                    this.digitando=true,
                    setTimeout(() => {this.digitando=false}, 2000
                    )
                }
            }
        }
    )
</script>