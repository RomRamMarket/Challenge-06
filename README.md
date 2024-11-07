# Challenge-06



<h1>Diferentes configuraciones necesarias para comenzar el proyecto.</h1>

<ol>
  <li>Sistema de input nuevo de Unity.</li>
  <li>Editor de código de su preferencia configurado en la configuración de su proyecto en Unity.</li>
  <li>Paquete de ProBuilder.</li>
  <li>Paquete "Sci-Fi Styled Modular Pack".</li>
  <li>Paquete "SciFi Warrior PBRHPP Polyart".</li>
  <li>Scripts configurados para que el jugador se mueva horizontal y verticalmente además de disparar al presionar click izquierdo.</li>
  
</ol>



<p> Comenzamos eligiendo un <code>Asset</code> de alguno de los paquetes que importamos para utilizarlo en el piso. A su vez le añadimos un <code>script</code> que se llame <code>floor</code>.</p>

<image
  src="challenge06/floor.png"
  width = 60%
  height = 60%>






<p>Duplicando los prefabs para tener en nuestro cuadrado <code>4x4</code>. Nuestra escena se vería asi:</p>


<image
  src="challenge06/preHecho.png"
  width = 60%
  height = 60%>



<p>Creamos un <code>Empty object</code> llamado <code>FloorManager</code> y para organizarlos ponemos todos los pisos bajo la jerarquía de este.</p>



<image
  src="challenge06/floorManager1.png"
  width = 30%
  height = 30%>





<p>También le añadimos un <Code>Script</Code> llamado <code>FloorManager</code>. Más adelante se encuentran las especificidades de este script.</p>



<image
  src="challenge06/floorManager2.png"
  width = 60%
  height = 60%>



<p>Repetimos un proceso similar, pero con las paredes. Elegimos el prefab del paquete que queremos utilizar para nuestras paredes. Además le añadimos un <code>Script</code> llamado <code>Life</code>. </p>


<image
  src="challenge06/pared2.png"
  width = 60%
  height = 60%>


  <image
  src="challenge06/pared1.png"
  width = 60%
  height = 60%>





<p>Para que pueda sensar las balas que impactan debemos añadir el <code>Rigid body</code> y marcar el encasillado de <code>Is Kinematic</code>. </p>



<image
  src="challenge06/pared3.rigid.png"
  width = 60%
  height = 60%>





<p>Creamos una esfera que será el prefab de nuestra bala del jugador y añadimos los siguientes componenetes.</p>


<image
  src="challenge06/bullet1.png"
  width = 50%
  height = 50%>




<p>En el script de <code>Contact Damager</code> realizamos los siguientes cambios.</p>

<image
  src="challenge06/contactDamager.png"
  width = 60%
  height = 60%>






<p>El scipt llamado <code>Floor Manager</code> tenemos este código para tener una lista en la que se encuentren todos los pisos.</p>



<image
  src="challenge06/floorManager.png"
  width = 60%
  height = 60%>








<p>Añadimos un método público para eliminar un piso aleatorio de la lista.</p>


<image
  src="challenge06/removeRandomFloor.png"
  width = 60%
  height = 60%>






<p>Para elegir de manera aleatoria el índice de la lista que le corresponde a cada pared, añadimos este código el script llamado <code>Life</code>.</p>



<image
  src="challenge06/life.png"
  width = 60%
  height = 60%>








<p>En esta animación puede verse en práctica como al dispararle a una pared se destruye un piso y al disparar a otra se destruye otro piso.</p>



<image
  src="ParedIndex.gif"
  width = 60%
  height = 60%>






<p>Repetimos en cierta medida el proceso de la pared ahora para que al impactar las esquinas se destruyan todos los pisos.</p>
<p>Elegimos prefab y añadimos componentes.</p>

<image
  src="challenge06/corner.png"
  width = 60%
  height = 60%>












<p>En el script <code>Contact Damager</code> añadimos el siguiente código.</p>




<image
  src="challenge06/corner2.png"
  width = 60%
  height = 60%>





<p>En el script <code>Life</code> añadimos el siguiente código.</p>

<image
  src="challenge06/corner3.png"
  width = 60%
  height = 60%>





<p>En el script llamado <code>Floor Manager</code> añadimos un método para que se eliminen todos los pisos al chocar con una esquina.</p>

<image
  src="challenge06/floorManager.corner4.png"
  width = 60%
  height = 60%>

<h2>Creando al enemigo</h2>

<p>Creamos el prefab del enemigo con todos sus componentes necesarios.</p>

<img src="img/Enemy1.png" width=80%, height=80%>

<p>Le damos un script al enemigo, llamado <code>Enemy</code>. Note que el <code>EnemyManager</code> aún no ha sido creado, pero no nos preocupemos por esto. ;) </p>

<img src="img/Enemy2.png" width=80%, height=80%>

<p>Añadimos otros scripts necesarios para el enemigo.</p>

<img src="img/Enemy3.png" width=80%, height=80%>
<img src="img/EnemyBonus.png" width=80% height=80%>

<h2>Manejando la aparición de los enemigos</h2>

<p>Ahora queremos crear los "spawners" de los enemigos para que aparezcan de diferentes posiciones y caminen en direcciones distintas. Además, crearemos un <code>Wave Manager</code> y un <code>Enemy Manager</code> que será importante posteriormente para manejar las condiciones de victoria y pérdida.</p>
<p>Creamos los "spawners"...</p>

<img src="img/EnemySpawner1.png" width=80% height=80%>
<img src="img/EnemySpawner2.png" width=80% height=80%>
<img src="img/EnemySpawner3.png" width=80% height=80%>
<img src="img/EnemySpawner4.png" width=80% height=80%>

<p>Creamos el <code>Wave Manager</code>...</p>

<img src="img/EnemySpawner5.png" width=80% height=80%>

<p>Asignamos los scripts correspondientes...</p>

<img src="img/EnemySpawner6.png" width=80% height=80%>
<img src="img/EnemySpawner7.png" width=80% height=80%>

<p>...y creamos el <code>Enemy Manager</code> con su script.</p>

<img src="img/EnemySpawner8.png" width=80% height=80%>
<img src="img/EnemySpawner9.png" width=80% height=80%>

<h2>"Make it rain!"</h2>

<p>Antes de mostrar el resultado, añadiremos otro toque especial a nuestro juego: ¡lluvia!
<p>Creamos un prefab que simulará una "gota" que caerá del cielo. Creamos su material y su prefab con las siguientes características:</p>

<img src="img/Rain1.png" width=80% height=80%>
<img src="img/Rain2.png" width=80% height=80%>

<p>Ahora, la parte más importante es lograr que las gotas de agua aparezcan rápidamente en <bold>distintas</bold> partes del mapa. Para esto, creamos un nuevo objeto vacío al que llamaremos <code>Rain Spawner</code>. Este se encargará de todas las gotas de lluvia.

<img src="img/Rain3.png" width=80% height=80%>

<p>Aquí creamos un script similar al del <code>Spawner</code> de los enemigos, pero con una adición: cada vez que se genera una gota, también se tiene que generar una posición aleatoria en su X y Z que se encuentre dentro del área del campo de batalla. A continuación, hay una implementación bastante simple de esta función:</p>

<img src="img/Rain4.png" width=80% height=80%>

<p>¡Veamos cómo cae la lluvia!</p>

![Rain](img/rain.gif)
