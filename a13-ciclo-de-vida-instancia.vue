<!DOCTYPE html>
<html>
    <head>
        <!-- Load Vuejs -->
        <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    </head>
    
    <body>
        <div id="app">
            <p>{{nome}}</p>
            <button v-on:click="alterarNome">Alterar Nome(Causa UPDATE do DOM)</button> <!-- esse evento renderizará a tela-->
            <button v-on:click="destruirInstancia">Destruir Instancia</button>
            <hr/>
            <p>beforeCreated = {{beforeCreated}}</p>>
            <p>created = {{created}}</p>
            <p>beforeMounted = {{beforeMounted}}</p>
            <p>mounted = {{mounted}}</p>
            <p>beforeUpdate = {{beforeUpdate}}</p>
            <p>updated = {{updated}}</p>
            <p>beforeDestroy = {{beforeDestroy}}</p>
            <p>destroyed = {{destroyed}}</p>

        </div>
        <script>
            app = new Vue (
                {
                    el: '#app',
                    data: {
                        nome: 'Jose',
                        beforeCreated: '*',
                        created: '*',
                        beforeMounted: '*',
                        mounted: '*',
                        beforeUpdate: '*',
                        updated: '*',
                        beforeDestroy: '*',
                        destroyed: '*',
                    },
                    methods: {
                        alterarNome() {
                            this.nome = 'Maria'
                        },
                        destruirInstancia() {
                            app.$destroy()
                        }

                    },
                    filters: {

                    },
                    computed: {

                    },
                    watch: {

                    },
                    // inicio das propriedade do ciclo de vida
                    beforeCreated() {
                        this.beforeCreated = 'executado'
                    },
                    created() {
                        this.created = 'executado'
                    },
                    beforeMounted() {
                        this.beforeMounted = 'executado'
                    },
                    mounted() {
                        this.mounted = 'executado'
                    },
                    beforeUpdate() {
                        this.beforeUpdate = 'executado'
                    },
                    updated() {
                        this.updated = 'executado'
                    },
                    beforeDestroy() {
                        this.beforeDestroy = 'executado'
                    },
                    destroyed() {
                        this.destroyed = 'executado'
                    },
                }
            )

        </script>
    </body>
</html>