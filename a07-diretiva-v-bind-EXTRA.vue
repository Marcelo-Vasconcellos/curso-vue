<!--
v-bind:attribute="expression";
Parâmetros: esta diretiva aceita a expressão que decidirá qual valor de atributo usar.

Exemplo: Este exemplo usa Vue.js para alternar as classes de um elemento com v-bind. Além disso, usaremos CSS para aplicar uma cor diferente a cada classe para que possamos vê-las mudando.
-->
<!DOCTYPE html>
<html>
  
    <head>
    
        <!-- Load Vuejs -->
        <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js">
        </script>
    
        <style>
            .active {
                color: blue;
            }
    
            .error {
                color: red;
            }
        </style>
    </head>
    
    <body>
        <div style="text-align: center;width: 600px;">
            <h1 style="color: green;">
                GeeksforGeeks
            </h1>
            <b>
                VueJS | v-bind directive
            </b>
        </div>
    
        <div id="canvas" style="border:1px solid #000000; width: 600px;height: 200px;">
    
            <!-- a DIV abaixo indica o processamento dos ventos Vue pela TAG id="app" -->        
            <div id="app" style="text-align: center; padding-top: 40px;">
                <!-- o evento v-on:click atribuirá diretamente o valor à variavel,
                     nesse exemplo não foi utilizado uma função para isso, a atribuição -->
                <button v-on:click="ifActive = !ifActive">Click para Mudar a Cor</button>
                <!-- v-bind associará o conteúdo da variável boolean definida em 
                    data: 'ifActive' atribuindo o valor de qual padrão CSS deverá ser utilizado-->
                <h1 v-bind:class="{active: ifActive, error: !ifActive}">
                    GeeksforGeeks
                </h1>
            </div>
        </div>
    
        <script>
            var app = new Vue({
                el: '#app',
                data: {
                    ifActive: true
                }
            })
        </script>
    </body>
</html>      