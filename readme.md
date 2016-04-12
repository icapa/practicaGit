- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**<br>
*git reset --hard HEAD*~1<br>
Porque quería volver al commit justo anterior y el *hard* porque quería forzar actualizar working copy
- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**<br>
*git reflog*
*git reset --hard c7de59e*<br>
Con reflog busco el commit al que quiero ir, cojo su identificador y hago un reset a ese punto forzando que se actualice working copy<br>
- **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**<br>
*git branch*
*git merge master*
Primero miro que estoy en rama styled, y luego hago el merge. No causó conflicto está actualizado porque los cambios que tiene styled son más nuevos
- **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?** 
*git branch styled*<br>
*git merge htmlify*<br>
Sí causó conflicto, el merge era no-ff y estaban modificadas las mismas líneas en los dos ficheros entonces git no sabe con cual quedarse, el usuario tiene que elegir<br>
- **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**<br>
*git checkout master*<br>
*git merge styled*<br>
No hay conflictos es un commit más nuevo, en la misma linea, hace un commit fast-forward, sólo mueve el puntero
- **¿Qué comando o comandos utilizaste en el paso 25?**
*git graph*
Tenía creado un alias para la representacion que me hace:git log --graph --decorate --pretty=oneline<br>
- **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**<br>
Sí puede ser fast forward porque se quiere hacer merge hacia un commit más avanzado, no hay que retroceder en el árbol.
- **¿Qué comando o comandos utilizaste en el paso 27?**<br>
*git reset HEAD~1*<br>
No es hard porque quiero mantener los cambios
- **¿Qué comando o comandos utilizaste en el paso 28?**<br>
Quiero descartar los cambios, me tengo que quedar con lo que hay
en staging area<br>
*git reset --hard HEAD*<br>
- **¿Qué comando o comandos utilizaste en el paso 29?**<br>
*git branch -D title*<br>
- **¿Qué comando o comandos utilizaste en el paso 30?**<br>
*git reflog*<br>
Con esto busco el nodo donde hicimos el merge
*git reset --hard 9126e51*
Con esto me muevo a ese commit y con hard porque quiero recuperar
- **¿Qué comando o comandos usaste en el paso 32?**<br>
*git reflog*<br>
Para conseguir el identificador del commit que quiero
*git reset --hard HEAD@{19}*<br>
Voy al nodo directamente y compruebo que el poema es el original<br>
- **¿Qué comando o comandos usaste en el punto 33?**<br>
*git reflog*<br>
Con eso busco el commit donde se hizo el merge con la rama title que incluía el título y luego
*git reset --hard 9126e51*
Voy a ese commit, compruebo que es el poema con el título<br>