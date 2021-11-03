# Typescript.__GB__
- es un lenguaje de programacion tipado 
- de alto nivel alto nivel de abtracion del codigo maquina
- genera como resultado codigo javascript
- codigo abierto
- se desarrolla en cualquier sistema operativo
- corre en cualquier navegador que corra javascript
- programacion Orientada a Objetos
- Potencia tu codigo Javascript
- Poderoso sistema de tipos
- compila a Es5 Es6 y mas
- es un proyecto muy activo/open sourse
- Actualizaciones periodicas
- comunidad creciente
- prevenir cerca de 15% de bugs
# instalacion de herramientas 
`-npm i -g typescript`
`-tsc -v` //vemos las version
# usar el compilador tsc
`mkdir typescrip/hello.ts
 cat                          console.log('hello typescript')`
`tsc hello.ts` //esto compila archivos js
`node hello.js`
- Usando el compilador tsc la opcion --watch
`tsc --watch hello.ts`//se mantiene escuchando los cambios

# Archivo de configuracion tsconfig.json
- espefica la raiz de nuestro proyecto Typescript
- permite configurar parametros para el compilador de typescript
- `tsc --init` //iniciamos el config.json
```json
{
"extends":"./configs/base",//?erencia de configuraciones
"compileOnSave":true, //? si queremos que ejecute la compilacion de manera automatica cuando guardemos cambios en nuestros archivos
"compilerOptions":{ //?configura las opciones de nuestro compilador
    "target":"es5", //?lo que se va a generar como resultado de compilacion
    "module":"commonjs", //?la configuracion para generar modules
    "strict":true, //?abilitar el checkeo de tipos estricto
    "removeComments":true //? eliminar los comentarios en el proceso de copilacion
    },
    "include":[
        "src/**/*.ts" //?los directorios que van a formar parte de lo que procesa el compilador
        ],
    "exclude":[
        "node_modules", //?lo archivos excluidos en el proceso de copilacion
        "**/*.test.ts" //?no se van a tomar en cuenta en el proceso de compilacion
        ]
        
}
```
# usando el archivo tsconfig.json
- `tsc --init` //iniciamos el config.json
- `tsc`// busca las configuraciones ./ y genera de forma automatica el archivo js


# clases
entidades relacones
# definiendo clases y consructores
```typescript
  enum PhotoIrientetion{
     lanscape,
     Portrait,
     Square,
     Panorama
  }
  
  //definir una clase
  class Picture {
     //propiedades
     id:number;
     title:
  }
```

# clases 
es una abtraccion de un conjunto de objetos
```typescript
enum PhotoOrientation{
  Landscape,
  Portrait,
  Square,
  Panorama
}

class Picture {
  //Propiedados
  id:number;
  title:string;
  orientation:PhotoOrientation;
  
  //en el construcctor definimos los atributos que se crean necesarios para poder dfefir nuestro objeto
  constructor(id:number,
               title:string,
               orientation:PhotoOrientacion,
               ){
               //this hace referencia a los distintos atributos que tiene nuestra clase
               this.id:id;
               this.title = title;
               this.orientation = orientation;
 }
 //comportamiento
 toId(){
    return `[id:${this.id}]`;
 }
```
# clases metodos set y get

# importando y exportando modulos
generalmente se define un modulo con la idea de agrupar codigo relacionado 
podemos tomar criterios en torno a la funcinalidad, feacture, utilitarios, modelos,etc
- import
- export

# Principio de responsabilidad Unica
un archivo deberia tener un proposito o responsabilidad unica: definir una clase, una interfaz, un enumerado, etc
esto mejora la legibillidad de codigo , y facilita su lectura, testing y favorece su mantenimiento

# resolviendo modulos
observando referencias relativas y no relativas
- classic [modulos amd,system,es2015] //poco configurable
- node [modulos commonJS o umd] //mas configurable

# webpack y agrupacion de modulos
empaquetador de modulos
- instalacion `npm i typescript wabpack webpack-cli`

