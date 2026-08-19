# Constructor del problema de investigación

Herramienta web interactiva para orientar a estudiantes de posgrado en la delimitación inicial de un problema de investigación. A partir de un recorrido guiado, la aplicación genera un planteamiento orientativo y tres rutas posibles de tesis, cada una articulada con su pregunta de investigación y objetivo general.

El proyecto está pensado como recurso de apoyo para un seminario de tesis. Sus resultados constituyen un punto de partida que debe revisarse mediante antecedentes científicos, criterios metodológicos y acompañamiento de la dirección de tesis.

## Archivo principal

- `Constructor_problema_investigacion_v2.html`: aplicación completa y autónoma.

Todo el diseño, la estructura HTML, los estilos CSS y la lógica JavaScript se encuentran integrados en este único archivo. No requiere instalación de dependencias ni conexión a una base de datos.

## Características

- Recorrido académico organizado en cuatro etapas.
- Validación de campos obligatorios antes de avanzar.
- Generación automática de un planteamiento orientativo del problema.
- Producción de tres opciones de tema con distintos alcances investigativos.
- Pregunta de investigación y objetivo general específicos para cada opción.
- Selección interactiva de la ruta de investigación preferida.
- Formulación diferenciada según el origen de la problemática.
- Descarga del resultado en formato de texto.
- Guardado automático de las respuestas en el navegador.
- Modo claro y modo oscuro.
- Diseño adaptable a computadoras, tabletas y teléfonos.

## Recorrido de la herramienta

### 1. Punto de partida

El estudiante registra:

- nivel académico;
- disciplina o programa;
- tema general de interés;
- experiencia o conocimiento previo relacionado.

### 2. Delimitación

Se define:

- fenómeno u objeto específico;
- personas, casos o materiales que funcionarán como unidad de análisis;
- contexto o lugar;
- periodo del estudio.

### 3. Problematización

La herramienta permite clasificar el origen del problema como:

- vacío de conocimiento;
- debate entre posturas;
- problema de la práctica.

Después solicita precisar qué se conoce, qué continúa sin resolverse y por qué resulta relevante investigarlo.

### 4. Viabilidad

El estudiante identifica:

- fuentes y datos disponibles;
- forma de acceso a la información;
- método o estrategia posible;
- tiempo y recursos reales.

## Resultados generados

La aplicación produce los siguientes componentes:

1. Planteamiento orientativo del problema de investigación.
2. Tres opciones de tema delimitadas.
3. Pregunta de investigación correspondiente a la opción seleccionada.
4. Objetivo general articulado con el tema y la pregunta.

Las dos primeras rutas mantienen una estructura estable:

- **Ruta descriptiva:** orientada a caracterizar el fenómeno.
- **Ruta analítica:** orientada a analizar factores asociados.

La tercera ruta se adapta al tipo de problemática elegido:

| Tipo de problemática | Orientación de la tercera ruta |
| --- | --- |
| Vacío de conocimiento | Condiciones y necesidades para comprender o desarrollar el fenómeno |
| Debate entre posturas | Comparación de perspectivas teóricas o empíricas |
| Problema de la práctica | Diseño de una estrategia fundamentada de mejora |

Esta correspondencia evita que el tema, la pregunta y el objetivo general respondan a alcances incompatibles.

## Cómo utilizar el código

1. Descargue `Constructor_problema_investigacion_v2.html`.
2. Abra el archivo con un navegador web moderno.
3. Complete las cuatro etapas del formulario.
4. Seleccione una de las tres rutas propuestas.
5. Revise la pregunta y el objetivo general asociados.
6. Utilice el botón **Descargar resultado** para conservar la propuesta en un archivo `.txt`.

También puede alojarse en un servidor web, campus virtual o repositorio institucional como cualquier página HTML estática.

## Tecnologías empleadas

- HTML5 para la estructura y los formularios.
- CSS3 para el diseño, los temas de color y la adaptación a diferentes pantallas.
- JavaScript nativo para la navegación, validación, generación de resultados y descarga.
- `localStorage` para conservar temporalmente las respuestas y la preferencia de color.

No utiliza bibliotecas, frameworks, servicios externos ni llamadas a una API.

## Privacidad y almacenamiento

Las respuestas se almacenan únicamente en el navegador del dispositivo mediante `localStorage`. El código no transmite datos a servidores externos. La información puede eliminarse desde la propia herramienta mediante el botón **Empezar de nuevo** o borrando los datos del sitio en el navegador.

## Personalización

### Colores

Los colores principales se encuentran declarados como variables CSS en `:root`:

```css
:root {
  --ink: #123d32;
  --orange: #ee6b29;
  --paper: #f6f2e9;
  --card: #fffdf8;
}
```

### Preguntas del formulario

Cada etapa está contenida en un bloque con el atributo `data-step`. Los campos obligatorios utilizan `data-required`.

```html
<div class="page" data-step="1">
  <!-- Campos de delimitación -->
</div>
```

### Lógica de generación

La función `build()` procesa las respuestas y construye:

- el planteamiento del problema;
- las tres rutas investigativas;
- las preguntas de investigación;
- los objetivos generales.

Para modificar las plantillas de redacción deben ajustarse los objetos almacenados en el arreglo `routes` dentro de esta función.

## Consideraciones académicas

- Las propuestas generadas son orientativas y no equivalen a un protocolo de investigación terminado.
- El estudiante debe comprobar la existencia de antecedentes, el vacío de conocimiento y la originalidad del tema.
- El método indicado por el usuario debe ser coherente con la pregunta, el objetivo y el tipo de datos disponibles.
- La redacción final debe revisarse con la dirección de tesis y adaptarse a las normas de la institución.
- La herramienta no sustituye la revisión de literatura ni la evaluación ética y metodológica del proyecto.

## Compatibilidad

Se recomienda utilizar una versión reciente de Chrome, Edge, Firefox, Safari u Opera. Algunas funciones, como copiar contenido al portapapeles o descargar archivos, pueden depender de los permisos configurados en el navegador.

## Estado del proyecto

Versión 2.0. La interfaz y el flujo principal se encuentran funcionales. Esta versión incorpora formulaciones académicas diferenciadas y mantiene la coherencia entre cada tema, su pregunta de investigación y su objetivo general.
