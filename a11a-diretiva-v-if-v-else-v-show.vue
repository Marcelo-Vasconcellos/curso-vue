<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<div id="app">
    <p v-if="mostrar">v-if Renderiza quando mostrar = true</p>   <!-- v-if (mostrar=true) renderiza, do contrário
                                                                não renderiza e não se inspeciona no DOM-->
    <p v-else>v-else Renderiza quando mostrar = false</p>          <!-- v-else (mostrar=false) renderiza, do contrário
                                                                não renderiza e não se inspeciona no DOM-->
    <p v-show="mostrar">v-show Rederiza quando mostrar = true</p>  <!-- v-if (mostrar=true) renderiza e aparece
                                                                na inspeção do DOM como oculta-->
    <button v-on:click="mostrar = !mostrar">Mostrar / Esconder</button> <!-- envento click definine valor da
                                                                                variável mostrar, a cada click
                                                                                alterna o valor entre
                                                                                true e false-->
</div>

<script>
    new Vue (
        {
            el: '#app',
            data: {
                mostrar:true
    
            },
            methods: {

            },
            filters: {

            },
            computed: {

            }

        }
    )
</script>