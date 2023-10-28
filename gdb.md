# Chasser les bugs avec gdb

Compiler le programme avec les infos de debug :

```
gcc -g -O0 [sources.cpp] -o a.out
g++ -o write_file_tbb write_file_tbb.cpp -ltbb
# ou
make DEBUG=y [monprog]   # si le Makefile est prévu pour ça

Puis démarrer le débuggeur :
```
gdb a.out
```

## Liste des commandes de base

Une fois dans gdb, le kit de survie :

| use |command |
|---|---|
| main breakpoint | break main |
| main function | break function |
| main line on cpp file | break fichier.cpp:ligne |
| start the program's execution | run |


```
     run
(c)  continue
(n)  next (tu déroules dans la même fonction et tu passes à la ligne suivante)
(s)  step (elle marche quand tu arrives à une ligne qui fait l'appel à une focntion)


(p)  print <variable>


(bt) backtrace
(f)  frame <N>
     up
     down

(l)  list
     edit
```