<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14"></script>

<div id="app">          <!-- tag de identificação para o Vue -->
    <h3>{{title}}</h3>  <!-- renderiza a variavel definida no Vue -->
    <p v-on:click="clickParagrafo">{{click}}</p> <!-- //diretiva v-on "escuta eventos" nesse caso um click no
                                                    Paragrafo e executa o método clickParagrafo-->
    <button v-on:click="clickButton">Alterar título</button> <!-- //diretiva v-on "escuta eventos" nesse caso
                                                              um click no Button e executa o metodo clickButton-->
</div>

<script>
    new Vue (
        {
            el: "#app",
            data: {
                title: 'Hello, World',
                click: 'não houve click'
            },
            methods: {
                clickButton() {
                    this.title = 'World, Hello',
                    this.click = 'Houve um Click no Button'
                },
                clickParagrafo() {
                    this.click = 'Houve um Click no paragrafo'
                }
            }
        }
    ) 
</script>