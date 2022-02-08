<!-- instala o Vue-->
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<div id="app">
    <p>{{texto1}}</p>
    <p>{{texto2}}</p>
    <input type="text" v-model="texto1">    <!-- apresenta  mesmo resultado que a diretiva v-on:input abaixo
                                                toda digitação é imediatamente refletida como conteúdo da variável
                                                texto1, podem ser ferificado o conteúdo de forma instantânea
                                            -->
    <input type="text" v-on:input="texto2 = $event.target.value">

</div>

<script>
    new Vue(
        {
            el: "#app",
            data: {
                texto1: '',
                texto2: '',                
            },
            methods: {

            },
        }
    )
</script>