# Silent Hill 3 Ammo Multiplier Patch



## Index 

| secciones/sections |  
| ------------- |
| [English version](#english-version) | 
|[Fair Use](#fair-use-disclaimer)    |
| [Principal](#principal-section)  | 
| [Installation](#installation-guide )  | 
| [Known Issues](#known-issues )  | 
| [Español](#version-en-español)  | 
| [Uso Justo](#descargo-de-responsabilidad)  | 
| [Seccion Principal](#sección-principal)  | 
| [Instalacion](#guía-de-instalación)  | 
| [Problemas Comunes](#problemas-comunes)  | 



## English version

### Fair Use Disclaimer
Silent Hill, Silent Hill 3, their characters, and all related content are properties of Konami and Team Silent. This is an unofficial patch and is neither worked on, promoted, nor distributed by Konami. Use at your own risk. This patch was created within the fair use framework to fix a bug in a software product that has been long abandoned and has not received official updates for more than 10 years. If you wish to obtain the game, please purchase it on Steam.

### Principal Section

The project originated as a way to circumvent a bug that nearly compromised my saved game during the final quarter, and as a means to level up my skills in reverse engineering. Having a keen interest in low-level programming and ambitions to become a malware analyst or game developer in the future, this project served as a practical learning tool. It was also born out of altruism for those who might encounter this bug in their game, given that there was no available fix, official or unofficial. However, my intention is not to support piracy but rather to encourage people to buy not only this particular game but also the entire Silent Hill series, and any game they enjoy, to support the game development industry.

This unofficial patch was created to fix a game-breaking bug in Silent Hill 3. It targets the Ammo Multiplier option which, due to a malfunction, can unintentionally reduce its value to 0, preventing the player from collecting ammo in the game. The mod was crafted using [Cheat Engine](https://cheatengine.org/) as a memory scanner and [xdbg64](https://x64dbg.com/) as a debugger/disassembler, some knowledge of assembly code [x86-64](https://www.amd.com/en/support/tech-docs/amd64-architecture-programmers-manual-volumes-1-5) was required to comprehend the game logic and write custom code to fix the problem.

The bug arises because the function designed to verify the value of the multiplier and adjust it if it falls below the minimum valid value or exceeds the maximum valid one does not actually perform that task. For those interested in understanding more about the technical side of the game-fixing process, please visit my blog article about it at: [blog]()

### Installation guide 

To install the patch just download the modified exe from the repository and  copypaste it in the game's folder to avoid any problem, save the old executable as sh3.exe.old just in case you need to restore the original game files.


### Known Issues

I could not make a perfect patch tho, there is a problem that basicaly consist of: while i check for the min and max values before changing the multiplier's value, the resulting behavior would reset the value to 1 even if you change the value to a valid on min-max range one, thus preventing you from using the multiplier in any value that it's not 1, like if the value was harcoded, wich may be a problem if you already completed the game, but in that case you can manualy change the value of the multiplier so there is no need to install the fix. This is due to a function call somewhere in the game's code, while i found all the static calls and jumps to the call instruction that executes our corrective function (as you may see in my blog explanation)  and also tried to manualy debug and set checkpoints to find any dinamic one (for example "call eax+123") for several hours. I could not find the one that its causing this problem, but as the patch still fixes the game breaking bug and since changing to normal game is as easy as replacing my executable for the original one. There is no big problem with it and you can enjoy the game anyway.

Wish you all a happy game session!

---

## Version en español

# Silent-Hill-3-Ammo-Multiplier-Patch

### Descargo de Responsabilidad 
Silent Hill, Silent Hill 3, sus personajes y todo el contenido relacionado son propiedad de Konami y Team Silent. Este es un parche no oficial y no ha sido desarrollado, promovido ni distribuido por Konami. Úsalo bajo tu propio riesgo. Este parche fue creado dentro del marco de uso justo para solucionar un error en un producto de software que ha sido abandonado hace tiempo y que no ha recibido actualizaciones oficiales durante más de 10 años. Si deseas obtener el juego, por favor cómpralo en Steam.

### Sección Principal

El proyecto surgió como una forma de resolver un error que casi arruino mi savegame durante el último cuarto del juego, y como medio para perfeccionar mis habilidades en ingeniería inversa. Ya  que siempre tuve un gran interés en la programación de bajo nivel y deseado de convertirme en analista de malware o desarrollador de juegos en el futuro, este proyecto sirvió como una herramienta práctica de aprendizaje. También nació de  altruismo para aquellos que podrían encontrar este error en su juego, dado que no había una solución disponible, oficial o no oficial. Sin embargo, mi intención no es apoyar la piratería, sino más bien alentar a las personas a comprar no solo este juego en particular, sino también toda la serie Silent Hill y cualquier juego que disfruten, para apoyar la industria del videojuego.

Este parche no oficial se creó para solucionar un error crítico en Silent Hill 3. Que afecta a la opción Ammo Multiplier que, debido a un mal funcionamiento, puede reducir su valor a 0 de manera no intencional, evitando que el jugador recoja municiones en el juego. El mod fue elaborado utilizando [Cheat Engine](https://cheatengine.org/s) como un escáner de memoria y [xdbg64](https://x64dbg.com/) como depurador/desensamblador, se necesitó cierto conocimiento de código de ensamblador [x86-64](https://www.amd.com/en/support/tech-docs/amd64-architecture-programmers-manual-volumes-1-5) para comprender la lógica del juego y escribir código personalizado para solucionar el problema.

El error surge porque la función diseñada para verificar el valor del multiplicador y ajustarlo si cae por debajo del valor mínimo válido o supera el máximo, en realidad no realiza esa tarea. Para aquellos interesados en entender más acerca del lado técnico del proceso de parcheo del juego, por favor visiten mi artículo de blog al respecto en: [blog]()

### Guía de Instalación 

Para instalar el parche, simplemente descarga el exe modificado del repositorio y cópialo en la carpeta del juego. Para evitar cualquier problema, guarda el ejecutable original como sh3.exe.old, por si necesitas volver a los archivos originales del juego.

### Problemas Comunes

A pesar de mis esfuerzos, el parche no es perfecto. Existe un problema en el que incluso si el codigo verifica los valores mínimos y máximos antes de cambiar el valor del multiplicador, el comportamiento resultante reinicia el valor a 1 incluso si cambias el valor a un rango mínimo-máximo válido. En consecuencia, esto te impide usar el multiplicador en cualquier valor que no sea 1, como si el valor estuviera harcodeado. Esto podría representar un problema si ya has completado el juego, pero en dicho caso puedes ajustar manualmente el valor del multiplicador, por lo que no tendrias necesidad de instalar el parche. Este problema se debe a una llamada de función en algún lugar del código del juego. Aunque localicé todas las llamadas estáticas y saltos a la instrucción de llamada que ejecuta nuestra función correctiva (como se detalla en mi explicación en el blog), e intenté depurar manualmente y establecer puntos de control para encontrar cualquier llamada dinámica (por ejemplo, "call eax+123"), no pude identificar al cambio de control culpable. Sin embargo, como el parche resuelve con éxito el error que rompe el juego y volver al juego normal es tan simple como reemplazar mi ejecutable con el original, no hay una gran preocupación. Todavía puedes disfrutar del juego.

¡Les Deseo a todos una alegre sesión de juego!
