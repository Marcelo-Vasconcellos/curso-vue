<!DOCTYPE html>
<html>
  
    <head>
    
        <!-- Load Vuejs -->
        <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js">
        </script>
    
        <style>
            .amarelo {
                background-color: yellow;
                color: blue;
            }
    
            .vermelho {
                background-color: yellow;
                color: red;
            }
        </style>
    </head>    
    <body>
        <div id="app">
            <input type="text" v-on:input="minhaCor = $event.target.value">
            <p v-bind:class="minhaCor">  <!-- a variavel minhaCor está sendo atribuida à CLASS via v-bind e
                                                quando a variavel coencidir com o Style CSS, as mudanças
                                                serão aplicadas.
                                                -->
                Classe CSS sendo aplicada = {{minhaCor}}
            </p>
        </div>
    </body>
    <script>
        new Vue(
            {
                el: '#app',
                data: {
                    minhaCor: '',
                }
            }
        )

    </script>
</html>