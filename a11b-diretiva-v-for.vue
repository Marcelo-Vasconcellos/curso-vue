<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>

<div id="app">
    <ul>
        <li v-for="minha_var, meu_indice in paises">{{meu_indice}} - {{minha_var.nome}} - {{minha_var.gpd}}</li>
        <!-- Renderiza uma lista completa, onde
            minha_var é referência do item atual para referenciar os elementos nome e gpd da lista
            meu_indice retorna número do index do elemento
            paises é o nome do array definido em data:, -->
    </ul>
</div>

<script>
    new Vue (
        {
            el: '#app',
            data: {
                paises:[
                {nome: 'Venezuela', gpd: 1},
                {nome: 'Brasil', gpd: 20},
                {nome: 'Japão', gpd: 30},
                {nome: 'Estados Unidos', gpd: 40},
                ]

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