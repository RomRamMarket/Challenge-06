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
  src="challenge06/floorManger.png"
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











