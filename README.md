# Calculadora-vectorial
  Calculadora Vectorial con visualizacion 2D / 3D

# Descripción
  Este proyecto es una aplicación web que permite realizar operaciones vectoriales entre hasta tres vectores (A, B y C) y visualizar los resultados en 2D o en 3D. Las operaciones disponibles incluyen:
    * -Suma de vectores
    * -Resta de vectores
    * -Cálculo del ángulo entre vectores
    * -Producto punto
    * -Producto cruz
    * -Producto triple `a⋅(b×c)`
    * -`a × ( b × c)`
    * -`(a × b) × c`
    - George Washington
    - George Washington
    - George Washington
  
  También permite elegir cómo visualizar el vector resultante, ya sea en un plano bidimensional o en un espacio tridimensional.
  
  La version en linea se puede ver en:
  https://tulitasrachet.github.io/Calculadora-vectorial/
  
  # Capturas y visualizacion.
  Al entrar en la aplicacion te aparecera de la siguiente manera.
  <img width="1868" height="917" alt="imagen" src="https://github.com/user-attachments/assets/88b3bbfb-a366-4392-8b6d-d578bf8179b2" />
  Algunos ejemplos:
  Angulo (2D)
  <img width="1872" height="911" alt="imagen" src="https://github.com/user-attachments/assets/d13b24ff-c5bc-4bdf-94ce-00f0847f134c" />
  Suma A+B (3D)
  <img width="1870" height="917" alt="imagen" src="https://github.com/user-attachments/assets/290917f8-4ca3-4e52-ba67-6485830fddca" />
  Producto punto (2D)
  <img width="1866" height="916" alt="imagen" src="https://github.com/user-attachments/assets/58837743-2d9b-407c-aa28-98cb0499b550" />
  
# ¿Como ejecutar?
  La calculadora se encuentra actualmente online, en el link: https://tulitasrachet.github.io/Calculadora-vectorial/ aunque si quieres correrlo de forma local tienes dos opciones.
  
      -Descargar el archivo.
        En el repositorio con link https://github.com/TulitasRachet/Calculadora-vectorial dale clic en el archivo index.html y ejecutalo desde tu computadora
      -Clonar el repositorio.
        Para este paso es necesario tener instalado git en tu computadora, despues de esto deberias ejecutar el programa y poner el siguiente comando "git clone https://github.com/TulitasRachet/Calculadora-vectorial", entra el directorio del proyecto con "cd Calculadora-vectorial", abre el archivo index en tu navegador de confianza.
        
  Empieza a usar la calculadora ingresando los valores de los vectores A, B, C y seleccionando una operacion y el modo de visualización.
# ¿Cómo funciona?
  -Estructura general
    -HTML
    
      Define la interfaz del usuario: campos de entrada, botones de operaciones y el área de visualización.
      -Contiene tres paneles principales.
        -Vector A (inputs para Ax, Ay, Az).
        -Vector B (inputs para Bx, By, Bz).
        -Vector C (unputs para Cx, Cy, By).
      -Botones que llaman a funciones JavaScript para cada operación.
      -Un panel donde muestra el gráfico ("#graph") y los resultados numéricos ("#result")
    -CSS
      -Le da estilo moderno con gradientes, botones de colores, sombras y bordes redondeados.
      -Mejora la usabilidad visual con animaciones en inputs y botones.
    -JavaScript
      -Implementa la lógica matemática de los calculos vectoriales.
      -Maneja la visualización de los vectores con Ploty.js en 2D y 3D
      -Guarda el último cálculo para poder alternar entre modos de visualización sin perder los resultados.
  -Funcionabilidad de las operaciones
  
    Cuando el usuario da clic en un botón, se ejecuta la función ("calculate(op)")que:
    
      -Obtiene los valores de los imputs de los vectores A, B y C.
      -Transforma esos valores en objetos con componentes {x, y, z}.
      -Dependiendo de la operación seleccionada, hace los cálculos:
        -Suma: A + B → muestra vector resultante.
        -Resta: A - B.
        -Ángulo: calcula el ángulo entre A y B usando el producto punto y magnitudes.
        -Producto Punto: A · B.
        -Producto Cruz A × B.
        -Producto Triple Escalar: A · (B × C)
        -Triple Vectorial.
          -A × (B × C)
          -(A × B) × C
      -Muestra el resultado numérico en el panel derecho.
      -Dibuja los vectores en la gráfica con ("plot(vectors, labels)")
   
    -Visualización con Ploty.js
      El sistema puede alternar entre 2D y 3D:
        -En 3D (scatter3d):
          -Se grafican los vectores desde el origen (0,0,0) hasta su extremo (x,y,z)
          -Se añade una escena con ejes X,Y,Z
        -En 2D
          -Se grafican solo los componentes X e Y
          -Perfecto para cuando los vectores están en el plano.
      El modo se cambia con los botones:
        -📉Ver en 2D → setMode(false)
        -📊Ver en 3D → setMode(true)
   
    -Flujo de uso del usuario
      -El usuario escribe los componentes de A, B, C.
      -Selecciona una operación (ej: Producto Cruz).
      -La calculadora:
        -Realiza la operacion en JavaScript.
        -Muestra el resultado en texto.
        -Grafica los vectores involucrados.
      -El usuario puede cambiar la visualización entre 2D y 3D.
