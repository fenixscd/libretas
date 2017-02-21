# JAVASCRIPT




## Recursos

[Pagina de jemplos](https://carlosazaustre.es/blog/ecmascript-6-el-nuevo-estandar-de-javascript/)






## Codigos de ejemplo
~~~
var obj = {  
    foo : function() {...},
    bar : function() {
        document.addEventListener("click", function(e) {
            this.foo();
        }.bind(this));
    }
}
~~~