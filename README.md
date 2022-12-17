Variables y operaciones
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
•	¿Qué es una variable y para qué sirve?
    Es un espacio en memoria, sirve para almacenar datos de difentes tipos.

•	¿Cuál es la diferencia entre declarar e inicializar una variable?
    Declarar un variable es simplemente nombrar la variable, inicializar una variable es asignarle un valor.

•	¿Cuál es la diferencia entre sumar números y concatenar strings?
    Para sumar numeros se necesitan valores de tipo number y contatenar es unir valores de difentes tipos dando como resultado un valor tipo string.

•	¿Cuál operador me permite sumar o concatenar?
    El operador de adición (+)

2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:
•	Nombre : String
•	Apellido : String
•	Nombre de usuario en Platzi : String
•	Edad : number
•	Correo electrónico : String
•	Mayor de edad : number
•	Dinero ahorrado : number
•	Deudas: number

3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
    - var nombre = "Yoel";
    - var apellido = "Barrios";
    - var usuario = "YoeL";
    - var edad = 26;
    - var correo = "yoel@mail.com";
    - var esMayorDeEdad = true;
    - var dineroAhorrado = 2000.00;
    - var deudas = 300.00;

4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
•	Nombre completo (nombre y apellido)
    console.log(nombre + " " + apellido);
•	Dinero real (dinero ahorrado menos deudas)
    console.log(dineroAhorrado - deudas);  

Funciones
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
•	¿Qué es una función?
    es un bloque de instruciones que sirve para realizar una tarea.

•	¿Cuándo me sirve usar una función en mi código?
    cuando se va realizar la misma tarea varias veces y los cambios solo seran los argumentos que le daremos a la funcion.

•	¿Cuál es la diferencia entre parámetros y argumentos de una función?
    los parametos son las variables que le asignamos a la funcion y los argumentos son los valores que le pasamos a la funcion.

2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:
    ```
    function datosPersonales(name, lastname, nickname){
        let completeName = name + ' ' + lastname;
        return "Mi nombre es "+completeName+", pero prefiero que me digas "+nickname+".";
    }

    console.log(datosPersonales("yoel", "barrios", "YoeL"));
    ```
Condicionales
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
•	¿Qué es un condicional?
    es una sentencia la cual debe ser evaluada si se cumple o no se cumple.

•	¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
    existen 3 tipos de condicionales if else, switch y el operador ternario.

    if ... else
    ```
    if (condición) {
    //código a ejecutar si la condición es verdadera.
    } else {
    //código a ejecutar si la condicion es falsa.
    }
    ```
    switch
    ```
    switch (condicion) {
    case 1:
        //ejecuta este código
        break;
    case 2:
        //ejecuta este código
        break;
    }
    ```
    Operador Ternario
    ```
    condicion ? bloque verdadero : bloque falso;
    ```

•	¿Puedo combinar funciones y condicionales?
    Sí, es posible combinar funciones y condicionales.

2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
    ```
    var tipoDeSuscripcion = "Basic";

    if(tipoDeSuscripcion == "free"){
        console.log("Solo puedes tomar los cursos gratis");
    }else if(tipoDeSuscripcion == "Basic"){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
    }else if(tipoDeSuscripcion == "Expert"){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    }else if(tipoDeSuscripcion == "ExpertPlus"){
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
    }
    ```
3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
    ```
    const tipoDeSuscripcion = "Basic";

    if(tipoDeSuscripcion == "free"){
        console.log("Solo puedes tomar los cursos gratis");
    }
    if(tipoDeSuscripcion == "Basic"){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
    }
    if(tipoDeSuscripcion == "Expert"){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    }
    if(tipoDeSuscripcion == "ExpertPlus"){
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
    }
    ```
- Usando arrays
    ```
    var tipoDeSuscripcion = "Basic";
    var tipoSuscripcion = [
        {
            suscripcion: "Free",
            acceso: "Solo puedes tomar los cursos gratis"
        },
        {
            suscripcion: "Basic",
            acceso: "Puedes tomar casi todos los cursos de Platzi durante un mes"
        },
        {
            suscripcion: "Expert",
            acceso: "Puedes tomar casi todos los cursos de Platzi durante un año"
        },
        {
            suscripcion: "ExpertPlus",
            acceso: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
        }
    ];

    var typeSuscripcion = tipoSuscripcion.find(function(suscription){
        return suscription.suscripcion === tipoDeSuscripcion;
    });
    console.log(typeSuscripcion);
    ```
- Usando Objetos
    ```
    const tiposDeSuscripciones = {
        Free: "Solo puedes tomar los cursos gratis",
        Basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
        Expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
        ExpertPlus: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
    }

    function conseguirTipoSuscripcion(suscripcion){
        if(tiposDeSuscripciones[suscripcion]){
            console.log(tiposDeSuscripciones[suscripcion]);
        }
    }
    conseguirTipoSuscripcion('Free');
    ```
Ciclos
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
•	¿Qué es un ciclo?
    Es una sentencia que se repite mientras se cumpla la condicion establecida.

•	¿Qué tipos de ciclos existen en JavaScript?
    for, while, do while.

•	¿Qué es un ciclo infinito y por qué es un problema?
    es un bucle que no termina nunca su ejecucion, el problema es que satura la memoria del ordenador.

•	¿Puedo mezclar ciclos y condicionales?
    Sí, es posible combinar ciclos y condicionales

2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:
    ```
    var i=0;
    while(i < 5){
        console.log("El valor de i es: " + i);
        i++;
    }

    var i=10;
    while(i >= 2){
        console.log("El valor de i es: " + i);
        i--;
    }
    ```
3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.
    ```
    function sumar(){
        var respuesta = prompt("Cuanto es 2 + 2 = ");
        if(respuesta == 4){
            console.log("Felicitaciones");
        }else{
            sumar();
        } 
    }
    sumar();
    ```
Listas
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
•	¿Qué es un array?
    Es un tipo de dato estructurado que permite almacenar una lista de elementos
    * Es un lista de elementos

•	¿Qué es un objeto?
    Es una coleccion de datos y funciones almacenados de forma asociativa.
    * Es una lista de elementos PERO cada elemente tiene un nombre clave.

•	¿Cuándo es mejor usar objetos o arrays?
    Usamos objetos cuando la coleccion de elementos de muy grande y de diferentes de tipos de datos, 
    y usamos arrays cuando tenemos una lista de datos especifica.

•	¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
    Sí, es posible combinar arrays con objetos o incluso objetos con arrays.

2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
    ```
    function primerValor(array){
        console.log(array[0]);
    }
    primerValor(['manzana', 'uva', 'mango', 'naranja']);
    ```
3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
    ```
    function todosLosElementos(array){
        for(let i = 0; i<array.length; i++){
        console.log(array[i]);
        }
    }
    todosLosElementos(['manzana', 'uva', 'mango', 'naranja']);
    ```
4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
    ```
    var fruta = {
        nombre: "Uva",
        color: "morado",
        forma: "Esferica",
        tamaño: "1,6 centímetros",
        platosFavoritos: ["chaufa", "tacos mexicanos"]
    };

    function todosLosElementos(objeto){
        //obtenemos las llaves del objeto
        let claves = Object.keys(objeto);
        for(let i=0; i< claves.length; i++){
            let valor = claves[i];
            console.log(objeto[valor]);
        }
    }

    todosLosElementos(fruta);
    ```
