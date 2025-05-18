# ARCH

## UNDO THE CHANGES MADE CHANGES MADE BY  THE PACMAN INSTALLER
Revertir cambios hechos con sudo
snapper ls: ver el stado de los snap
snapper status 1..2: ver las modificaciones entre uno y otro
sudo snapper undochange x..y: pasa los cambios que hay en y a x(si x es una versión antes elimina los paquetes instalados - y..x revierte eso)

## UNDO  ANY CHANGES MADE TO INDIVIDUAL FILES
snapper no solo permite deshacer todos los cambios entre dos snapshots, sino que también permite
restaurar un solo archivo
sudo snapper undochange x..0 /dir/file: cambia todos los valores del archivo

## CREATE MANUAL PRE-POST SNAPSHOTS AND UNDO THE CHANGES
snapper -c homre ls: para ver otros snap guardados
snapper -c root create -t pre -c number -d 'mensaje': crea un snapshot manual en root(modificar root por home o por la division que quiera)
snapper -c root create -t post --pre-number "numero al que está enlazado el pre" -c number -d 'post modificacion': crea un snapshot post
snapper status x..y | wc -l: cantidad de archivos instalados
snapper -c root delete x: eliminar(cambiar root por la seccion que quiera)

## ROLLBACK TO A PREVIOUS SNAPSHOT FROM THE GRUB MENU

