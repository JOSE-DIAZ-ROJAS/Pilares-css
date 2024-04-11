PILARES DE CSS
[SELECTORES]:
    1. SELECTOR UNIVERSAL: Se aplica a todos los elementos del documento ==> *{}
    2. SELECTOR DE ETIQUETA:  Coicide con los nombres de los elementos. ==> p{}
    3. SELECTOR DE CLASE: En este caso se selecciona  el elemento usando la clase asignada a 
       dicho elemento.    ==>   .clase{}, son los mas usados ya que permiten hacer CSS reutilizable
    4. SELECTOR DE IDENTIFICACION ==> Se usa el identificador para seleccioanr un elemnto  #ident{}

    5. SELECTOR DE ATRIBUTO
        5.1 Atributo ==>  ["atributo"]{}
        5.2 Atributo= valor==> [atributo="valor"]{}
        5.3 Si empieza por el valor "x" ==> [atributo^="valor"]{}
        5.4 Si contiene el valor "x" ====> [atributo*="valor"]{}
        5.5 Si termina con el  valor "x"==> [atributo~="valor"]{}

    6. SELECTORES AGRUPADOS ===>si vamos a dar los mismos estilos a varios elementos (ejemplos)
            .text-1,
            .text-2,
            .text-3{
            background-color: antiquewhite;
            }
            
            p , h1{
            color: red; font-family: Arial, Helvetica, sans-serif;
            }

    7. SELECTOR DE HIJOS (descendiente) (Se separa con espacio y se recomienda bajar un solo nivel) (se puede combinar con todos los selectores estudiados), ejemplos:

            div .title-sec{
                background-color: yellowgreen;
            }
            div h2{
                background-color: yellowgreen;
            }
            div #ident{
                background-color: yellowgreen;
            }
            div [atributo]{
                background-color: yellowgreen;
            }

    8. SELECTOR DE HERMENO SIGUIENTE (se puede hacer con los selectores clase, etiqueta, etc)

            .text-4 + .title-1{
                color: rgb(107, 21, 187);
            }

            .text-4 + h2{
            color: rgb(107, 21, 187);  
            }
            .text-4 + [atributo]{
            color: rgb(107, 21, 187);  
            }
    9. SELECTOR DE TODOS LOS HERMANOS SIGUIENTES

             (por clase)
            h3~ .text-5{
            color: rgb(24, 192, 38);
            }

            (por etiqueta)
            h3~p{
            color: rgb(24, 192, 38);
            }
    10. SELECTOR DE HIJOS DIRECTOS (solo selecciona a los hijos directos de un elemento, se puede hacer con todos los selectores vistos anteriormente)

    .container> p{
       background-color: rgb(214, 162, 162);
       }
       

[HERENCIA]: ES la capacidad que tienen algunos elementos de heredar alguanas propiedades,de sus elementos contenedores (padres, abuelos,etc) Ejem.

.dia{

    color: rgb(209, 22, 62); font-size: 20px;
  }

  Nota: los enlaces no heredan propiedades, pero se puede forzar al herencia con el siguiente:
  .link{
      color: inherit;
  }
  Nota:Con el  valor "initial" hecemos que ciertos elemento no hereden la propiedad en mension.
  .lab{
    color: initial; 
  }

[CASCADA] : El ultimo selector sobre escribe a  los primeros  que hagan referencia a un elemento  determinado.


[ESPECIFICIDAD] : Es el grado de importancia que tienen los selectores, para aplicar las propiedades.

¿Como funciona css?

selector de etiqueta/ pseudoelementos         : 0001
selector de clases/atributos/pseudoclases     : 0010
selector  de id                               : 0100
selector inline                               : 1000
inportant                                     : infinito, No se recomienda usar important para un css limpio

  