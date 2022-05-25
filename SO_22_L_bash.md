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