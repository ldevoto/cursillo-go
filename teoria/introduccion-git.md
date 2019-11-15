## Qué es Git?
> Git es un sistema de control de versiones distribuido gratuito y de código abierto diseñado para manejar todo, desde proyectos pequeños hasta muy grandes, de manera rápida y eficiente.

La anterior es la definición textual sacada de la página de [Git](https://git-scm.com/). Es muy bonita, concisa y correcta y para el que sabe, describe a la perfección lo que es. Pero... qué pasa con el que nunca escuchó hablar de Git? Qué pasa con el que no entiende ni una sola palabra de lo anterior?

Git es una herramienta fundamental para todo desarrollador hecho y derecho. Git permite, mediante comandos sencillos, manejar las diferentes versiones de nuestro proyecto a lo largo del tiempo.

A todos nosotros en algún momento de nuestra vida estudiantil o profesional, nos han asignado una tarea que debía completarse en tiempo y forma y cumpliendo ciertos requisitos. Pongamos el ejemplo de un Trabajo Práctico, por ahora, individual que nos piden en la facultad.
El TP debe ser entregado dentro de dos semanas y debe responder a 4 items (no vienen al caso cuáles son esos items).
Cómo lo resolveríamos?
Veamos una posible linea temporal de cómo cumplir con lo pedido
- Comenzamos creando un documento llamado `TP-materia.doc`
- Copiamos las preguntas o items al documento y guardamos
- Empezamos a resolver algunos items
- Ya es tarde por lo que guardamos el documento y nos vamos a dormir
- Al día siguiente, siendo un día laborable, nos encontramos con que si queremos seguir avanzando con el TP, debemos llevárnoslo en algún pendrive o mandarnos un mail con el documento
- Decidimos copiarnos el documento al pendrive y seguir desde el trabajo
- En el trabajo trabajamos con el documento (todo lo posible) y guardamos los cambios
- Cuando volvemos a casa, queremos seguir avanzando pero para hacerlo tenemos que decidir con que version seguir. Podemos seguir con la que está en nuestra PC o con la que trajimos del trabajo (donde borramos cosas que estaban originalmente, agregamos varias mas pero todo en un ambiente "a las escondidas")
- Entonces tenemos que elegir. Decidimos conservar ambos archivos (por las dudas) llamando a la versión del trabajo TP-materia-trabajo.doc
- Seguimos avanzando desde el TP del trabajo.
- Al día siguiente nos pasa lo mismo. Volvemos a copiar la ultima version al pendrive, la trabajamos en el trabajo y cuando volvemos a casa debemos elegir que conservar.
- Decidimos conservar todo. Así, al cabo de 5 días tenemos varias versiones del mismo documento `TP-materia-trabajo.doc`, `TP-materia-trabajo1.doc`, `TP-materia-trabajo2.doc`, `TP-materia-trabajo3.doc`, etc.
- Al final de la semana tenemos nuestra versión final del documento llamada `TP-materia-final.doc` conformada por partes de todas las versiones. Algunas con cosas repetidas, otras no.
- Llega el día de la entrega y nos damos cuenta que nos faltó completar un párrafo y agregarle una carátula. Como no queremos perder nada, agregamos lo que nos falta y llamamos al nuevo documento final, `TP-materia-final-entregable.doc`
- Antes de entregar nos damos cuenta que la versión final que íbamos a entregar, está incompleta. Sin querer borramos dos párrafos y no nos dimos cuenta. Agradecemos haber conservado la version pre-final.
- Creamos una nueva versión con la carátula y el párrafo que agregamos de la version entregable y todo el resto de la version final. Al finalizar tenemos nuestra ultima versión que es `TP-materia-final-entregable-real.doc`

Es un ejemplo largo pero vale la pena ver que realmente es lo que sucede. A quién no le pasó? Que sin darse cuenta uno termina con muchas versiones (todas intermedias y conservadas por las dudas) de las cuales una sola es la que realmente le será útil.

No sería bueno tener una herramienta que nos ayude con este problema?
SI! Y para eso está Git. 

El ejemplo anterior explica una parte de la definición de qué es Git
> Git es un sistema de control de versiones

Cuando se habla de control de versiones, se habla de delegar a la herramienta la administración y guardado de las distintas versiones de un documento o conjunto de documentos.

Git, luego hace mención a lo distribuido
> Git es un sistema de control de versiones distribuido

Y a qué apunta con eso? Muy sencillo, qué pasaría si en lugar de ser un TP individual, fuera un TP grupal?
Las versiones de los documentos ya no los maneja solo uno. Depende del resto de los compañeros también. Las cosas que agreguen y saquen solo las van a saber ellos y si uno no confía en sus compañeros va a pasar muchas horas viendo que cosas cambiaron cada uno y si era correcto o no. Además que la cantidad de versiones con las que se va a contar al final, va a ser mucho mayor ya que cada integrante del TP va a hacer sus cambios en su versión generando muchos mas nombres del estilo `TP-materia-integrante-1,2,3,4.doc`

Sigue hablando de gratuito y de código abierto
> Git es un sistema de control de versiones distribuido gratuito y de código abierto

Ambas se explican casi solas. Gratuito nos habla de que para usarlo no hay ningún costo, es completamente gratis. Y de código abierto quiere decir que uno puede ver como está hecho, osea, uno puede ver el código fuente de Git.

Todo esto nos lleva de nuevo a tener que preguntarnos, qué es Git?
Y bueno, la respuesta más amigable teniendo en cuenta lo que se dijo anteriormente sería: 
#### Git es una herramienta que nos permite administrar, mediante comandos simples, diferentes versiones de un proyecto a lo largo del tiempo, en forma colaborativa, conservando el qué, cuándo y por qué de los distintos cambios de versiones, pudiendo reconstruir la historia en todo momento sin inconsistencias ni dualidades. 

Para más detalle se puede consultar la siguiente página que contiene [4 videos](https://git-scm.com/videos) explicando más en detalle esto mismo.

## Qué puedo hacer con Git?
Con Git se puede
- Crear un repositorio para comenzar a traquear archivos (ver `git init`)
-  Agregar archivos a un repositorio para comenzar a ser versionados (ver `git add`)
- Agregar nuevas versiones de documentos o archivos al mismo repositorio con mensajes indicando los cambios (ver `git commit`)
- Conocer el estado de nuestro repositorio local en todo momento (ver `git status`)
- Subir nuestros repositorios a una plataforma web con un servidor git centralizado (como [GitHub](https://github.com/)) para que sean accesibles desde cualquier computadora con conexión a internet (ver `git push`)
- Actualizar un repositorio local con el contenido del repositorio remoto de la web (ver `git pull`)
- Bajar a nuestra PC un repositorio remoto existente por primera vez (ver `git clone`)
- Volver a una versión anterior o a otra linea temporal de un documento o de todo el repositorio (ver `git checkout`)
- Crear lineas de tiempo paralelas con diferentes versiones del mismo archivo (ver `git brach`)
- Unir dos o más lineas de tiempo paralelas en una misma (ver `git merge`)

## Qué comandos Git existen?
- `git init`
	- Inicializa un repositorio Git en el directorio donde se ejecute el comando.
- `git status`
	- Indica el estado actual de nuestro repositorio local. Podemos ver los archivos que no se están traqueando, los que hayan cambiado desde el último versionado o si todo está en su ultima versión. (**NO** nos brinda información sobre el repositorio remoto, osea, si queremos saber si hay cambios en el repositorio remoto, debemos usar otros medios)
- `git diff`
	- Si el comando `git status` nos mostrara que hay archivos cambiados con respecto a la última versión commiteada, usando este comando podemos ver qué cambió en concreto en cada archivo.
- `git add <file/directory>`
	- Permite indicar qué archivos o directorios `<file/directory>` se quieren agregar a la próxima versión.
- `git commit -m "<mensaje>"`
	- Agrega los archivos anteriormente marcados para agregar a una versión con el `<mensaje>` indicado.
- `git push`
	- Sube los cambios en nuestro repositorio local al remoto. (Hay que configurar a que repositorio remoto lo vamos a subir solo la primera vez)
- `git pull`
	- Baja los cambios que estén en el repositorio remoto a nuestro local. Si hay algún conflicto intentará resolverlo solo. Si no puede resolverlo solo, tendremos que arreglar todos los archivos con conflictos a mano y luego proceder a hacer un `git add <archivosConflictivos>` y `git commit` para crear la versión con los conflictos solucionados.
- `git clone`
	- Clona un repositorio remoto en nuestra PC y nos deja el repositorio en la versión más nueva por defecto.
- `git checkout`
	- Podemos ir moviéndonos entre versiones de un archivo, del repositorio, entre diferentes lineas de tiempo y demás. 
- `git branch`
	- Brinda información sobre la linea de tiempo en la que estamos parados. Las lineas de tiempo en Git se las llama `branch` o `rama` en español.
- `git merge`
	- Une dos o más lineas de tiempo/`branch`/`rama` en una sola en nuestro repositorio local.


## Cómo es un flujo habitual de trabajo con Git?

1. Si estamos creando un nuevo repositorio y queremos subirlo a GitHub
```bash
# Inicializamos el repositorio local parados en el directorio con el proyecto
> git init

# Verificamos el estado de nuestro repositorio local
# (Siempre es una buena práctica chequear el estado y ver que archivos tocamos)
> git status

# Agregamos todo el contenido del directorio para versionar
> git add .

# Commiteamos todo lo agregado anteriormente con una descripción pertinente
> git commit -m "Descripción de los cambios commiteados"

# Vinculamos nuestro repositorio local a uno remoto (previamente creado)
> git remote add origin <urlDeSuRepositorioRemoto>

# Por única vez pusheamos con este comando todo nuestros cambios al repositorio remoto (posteriormente con solo hacer "git push" alcanza)
> git push -u origin master
```

2. Si estamos queriendo bajar un repositorio de GitHub y trabajar con el
```bash
# Nos clonamos el repositorio remoto a nuestra PC
> git clone <urlDelRepositorio>

# Nos movemos dentro del directorio del proyecto que nos acabamos de bajar
> cd <nombreDelProyecto>

# Hacemos todos los cambios que necesitemos
# (Solo a modo de ejemplo creo un archivo de texto)
> echo "hola mundo" > archivo_nuevo.txt

# Verificamos el estado de nuestro repositorio local
# (Siempre es una buena práctica chequear el estado y ver que archivos tocamos)
> git status

# Agregamos todo el contenido del directorio para versionar
> git add .

# Commiteamos todo lo agregado anteriormente con una descripción pertinente
> git commit -m "Descripción de los cambios commiteados"

# Pusheamos nuestros cambios commiteados al repositorio remoto.
# Si hubiera cambios en el repositorio remoto que no tenemos, nos va a fallar el comando y vamos a tener que hacer un "pull" antes del "push"
# Si el repositorio que nos bajamos no es nuestro y no tenemos permisos de escritura en el mismo, el "push" nos va a fallar (y con razón)
> git push
```

3. Si estamos trabajando con un repositorio ya vinculado y existente en nuestra PC
```bash
# Bajamos todos los cambios nuevos que hayan en el repositorio remoto 
# (si somos los únicos no es necesario hacer esto ya que no habrán nuevos cambios, aunque es una buena práctica para asegurarse de que estamos al día)
> git pull

# Verificamos el estado de nuestro repositorio local
# (Siempre es una buena práctica chequear el estado y ver que archivos tocamos)
> git status

# Agregamos todo el contenido del directorio para versionar
> git add .

# Commiteamos todo lo agregado anteriormente con una descripción pertinente
> git commit -m "Descripción de los cambios commiteados"

# Pusheamos nuestros cambios commiteados al repositorio remoto.
# Si hubiera cambios en el repositorio remoto que no tenemos, nos va a fallar el comando y vamos a tener que hacer un "pull" antes del "push"
> git push
```
