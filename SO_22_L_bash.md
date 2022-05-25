```bash
# print arguments in command line

#!/bin/bash
for i; do 
   echo $i 
done

#!/bin/bash
while (( "$#" )); do 
  echo $1 
  shift 
done

# print the command line arguments that are files

#!/bin/bash
for i in "$@"
do
        if [ -f $i ]
        then
         echo $i
        fi
done

# print the command line arguments that are writable files

#!/bin/bash
for i in "$@"
do
        if [ -f $i ] && [ -w $i ]
        then
         echo $i
        fi
done

# copy the command line arguments that are writable files in 'writable' folder

#!/bin/bash
cale="writable/"

for i in "$@"
do
        if [ -f $i ] && [ -w $i ]
        then
         echo $i
         cp $i $cale
        fi
done

# la testare
# de schimbat drepturile la un fisier, copiere si creare de fisiere (windows si linux)
```

- `chmod 777 nume_script.sh` - modificare permisiuni fisier cu `chmod` 
- afisare argumente linie comanda, afisare prim argument, afisare fisierele txt de la folderul dat ca arg, afisare pentru fiecare fisier txt din folder dat ca argument linie comanda numarul de linii, copiat fisierele date ca argument in alt folder daca acestea au permisiune de execute.
- Cum se foloseste while (cu shift) si for: https://linuxconfig.org/how-do-i-print-all-arguments-submitted-on-a-command-line-from-a-bash-script