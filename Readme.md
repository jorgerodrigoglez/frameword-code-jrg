# SASS framework

### Configuración:

#### settings.scss


### Breakpoints



### Nomenclatura


### Organización


### Gulp


#### Instalación
Se necesita tener instalado Nodejs (https://nodejs.org/en/) y Gulp:
`npm install gulp -g`

Una vez instalados los requisitos anteriores se ejecuta:
`npm install`
en el raíz del proyecto. Esto instalará todas las dependencias para que Gulp pueda compilar Sass.

#### Actualizar dependencias

Las dependencias están continuamente actualizándose, una buen método para automatizar esta tarea es utilizar ```npm-check-updates```

```sh
npm install -g npm-check-updates
```

Ahora ejecutamos en el terminal el siguiente comando para actualizar todas las dependencias.

```sh
ncu
```

El terminal nos informará de las dependencias que se han actualizado.

```sh
autoprefixer     ^6.0.3  →  ^6.1.2
gulp-minify-css  ^1.2.1  →  ^1.2.2
```

#### Configuración y uso
Para configurar gulp podéis entrar a `gulpfile.js` y modificar el json de configuración (primeras líneas):
```
config = {
  autoprefixer : true, //Prefijos de navegadores para CSS: compatibilidad con browsers
  minify : true, // Minificado de CSS
  mergeMediaQueries: true, // Unimos el interior de las mediaQueries con las misma condición
  paths : {
    ...
  }
}
```
**Tarea autoprefixer** (true o false): tras compilar el `.scss` añade prefijos de navegadores para mejorar la compatibilidad con estos.
**Tarea minify** (true o false): tras compilar el `.scss`, minificamos el css, borrando todos los espacios innecesarios y comentarios.
**Tarea mergeMediaQueries** (true o false): tras compilar el `.scss`, unificamos todas las mediaqueries con la misma condición, lo cual es perfecto para combinar con el mixing `respond-to()`.

Nota: todas las tareas se pueden combinar como se desee.

Para hacer que gulp compile nuestro `.scss` debemos escribir `gulp` en consola.

## Patrones

