#   Practica3. Etiquetar commits y ver diferencias.

En esta actividad vamos a ver 3 comandos:

-git tag
-git show
-git diff

El primer comando (git tag) nos permite poner etiquetas a los commits.

Los 2 siguientes (git show y git diff) son para ver los cambios realizados entre distintos commits. Son muy parecidos aunque con pequeñas diferencias.

Básicamente git show nos permite ver los cambios de un commit respecto al anterior, mientras que git diff nos permite ver cambios en un rango de commits.**


# 1. Etiquetamos el commit primero y el tercero.

El primer commit será la versión 1 de nuestro proyecto. La etiqueta será v1.

El tercer commit será la versión 2 de nuestro proyecto. La etiqueta será v2.

El segundo commit no será etiquetado.

Para etiquetar utilizamos el comando
git  tag  -a  nombre_etiqueta  -m  "Mensaje"   commit_a_etiquetar

Por ejemplo, en mi caso:

git tag  -a v1  -m "Eliminar inicio"  b7ec

![](https://github.com/zazi479/practica3/blob/cecbc2caf4a7c14777045e1e1f140592ec7b2f36/cap2.jpg)
![](https://github.com/zazi479/practica3/blob/cecbc2caf4a7c14777045e1e1f140592ec7b2f36/cap3.jpg)

git tag  -a v3  -m "Eliminar tercero "  7c5f
![](https://github.com/zazi479/practica3/blob/cecbc2caf4a7c14777045e1e1f140592ec7b2f36/cap4.jpg)
![](https://github.com/zazi479/practica3/blob/cecbc2caf4a7c14777045e1e1f140592ec7b2f36/cap5.jpg)

La opción -a significa annotate.

La opción -m nos permite poner un mensaje.

Finalmente debemos poner el commit al que deseamos aplicar la etiqueta.

Si por cualquier motivo nos equivocamos al crear la etiqueta podemos eliminarla con

git tag -d nombre_etiqueta


# 2. Usando etiquetas para movernos

Las etiquetas nos permiten referenciar commits de una forma más cómoda que usando el identificador de hash.

Por ejemplo es más cómodo usar:

git checkout v1

![](https://github.com/zazi479/practica3/blob/7f92cabcec37a0c2b299ae8590b070a02175b463/cap6.jpg)

que usar

git checkout 7c5f


Para volver al último commit haz

git checkout master

# 3. Examinado cambios de un commit respecto al anterior.

![](https://github.com/zazi479/practica3/blob/1d8fb918c8ec6c6e396f17f0a430338d59b28462/cap7.jpg)

Para ver los cambios introducidos respecto al commit anterior hacemos:

git show
En este caso, al coincidir todos los apuntadores (HEAD, master, v2 y fdeb) al mismo sitio, el comando anterior es equivalente a

git show HEAD
git show master
git show fdeb
git show v3

![](https://github.com/zazi479/practica3/blob/2e4164959707e8239297bbccfdbef98275a3ccbc/cap8.jpg)

En mi caso nos indica cuando se elimino este aechivo.


En otro caso si añades una linea,nos aparecerá en verde y con un signo +.Y las líneas eliminadas aparecen en rojo y con un signo -.
![](https://github.com/zazi479/practica3/blob/f11da6946e25f03686d3085d07c4d0c25c63a686/cap8.1.jpg)


En este caso sólo hemos realizado operaciones de adicción.


# 4. Examinado cambios de un commit respecto a varios anteriores.

Si deseamos ver todos los cambios realizados a lo largo de varios commits, haremos uso de git diff.

La forma de uso es

git  diff  commit1..commit2
Por ejemplo, para ver los cambios entre la versión 1 y la versión 2, hacemos

git  diff  v5..v4
![](https://github.com/zazi479/practica3/blob/f11da6946e25f03686d3085d07c4d0c25c63a686/cap9.jpg)

Podemos ver que se han añadido 1 líneas desde el commit v5.

Es muy aconsejable poner primero el commit más antiguo y después el commit más moderno. Si lo hacemos al contrario, el resultado en lugar de aparecer en color verde aparecerá en color rojo, y su interpretación será más confusa.



# 5. Diferencia entre git show y git diff

También podemos hacer

git show v5..v4

![](https://github.com/zazi479/practica3/blob/15a7cb88c2783636048d15488d522078f48ab074/cap9.1.jpg)

La direncia entre el comando git  diff  v5..v4 y el comando git show v5..v4 es  la siguiente:
el comando git show nos especifica la fecha y el autor que lo ha realizado.
![](https://github.com/zazi479/practica3/blob/53094030e31f18cfff5c2dd354979f12d93b6366/CAPTU.jpg)




