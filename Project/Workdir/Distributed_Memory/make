#!/bin/bash

for (( i=0; i<$1; i++ ))
do
sed 's/define N 6/define N '$1'/g' node$i.c | sed 's/define current_node_number 0/define current_node_number '$i'/g' > temp$i.c
gcc temp$i.c -o temp$i.o
chmod +x temp$i.o
gnome-terminal -- ./temp$i.o -t "Node $i"
rm temp$i.c
done
