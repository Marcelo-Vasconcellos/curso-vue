<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14"></script>

<div id="app">
    <span v-text=titulo1></span>    <!-- anula rederização html(se houver), como descaracterizar um texto de link entre outros-->
    <span v-html=titulo2></span>    <!-- renderiza o texto aplicando instruções html que sejam injetadas no texto-->
    {{titulo3}}                     <!-- rederiza o texto apresetentado -->
    <button v-on:click="b1">Normal</button>     <!-- escuta um click, e executa a função b1 -->
    <button v-on:click="b2">Aumenta 1</button>  <!-- escuta um click, e executa a função b2 -->
    <button v-on:click="b3">Aumenta 2</button>  <!-- escuta um click, e executa a função b3 -->
</div>

<script>
    new Vue(
        {
            el: '#app',
            data: {
                titulo1: '<h3>Meu Títilo1</h3>',
                titulo2: '<h3>Meu Títilo2</h3>',
                titulo3: '<h3>Meu Títilo3</h3>',
            },
            methods: {
                b1: function() {
                    this.titulo2 = '<h3>Meu Títilo2</h3>'
                },
                b2: function() {
                    this.titulo2 = '<h2>Meu Títilo2</h2>'
                },
                b3: function() {
                    this.titulo2 = '<h1>Meu Títilo2</h1>'
                }
                
            }

        }
    )

</script>