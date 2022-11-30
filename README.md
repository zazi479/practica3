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

git checkout 8b67


Para volver al último commit haz

git checkout master

# 3. Examinado cambios de un commit respecto al anterior.

![]()
![]()
![]()
![]()
