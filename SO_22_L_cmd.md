## CMD

### Comenzi uzuale

- `dir` - afiseaza continutul folderului
- `tree` - afiseaza ierarhic continutul folderului
- `cd foldername/path` - inainteaza catre `foldername/path`
- `cd ..` - se intoarce la folderul parinte
- `cd ../..` - se intoarce la folderul bunic (parinte al parintelui/2 foldere in spate)
- `mkdir foldername` - creeaza un nou folder cu numele `foldername`
- `rmdir foldername` - sterge folderul cu numele `foldername`
- `echo param` - afiseaza `param` in consola

### Creearea de noi fisiere
- `echo content > test.txt` - creaza fisierul `test.txt` ce contine `content`
- `copy con test.txt` - dupa introducerea comenzii, se apasa `Enter`, se introduce continutul fisierului, daca se doreste o noua linie se apasa `Enter`, apoi `Ctrl+Z` pentru a inchide scrierea si `Enter` pentru salvare
- `copy nul test.txt`- creeaza un fisier gol
- `type nul > test.txt` - creeaza un fisier gol
- `notepad test.txt` - deschide Notepad si implicit cere creearea unui nou fisier, daca `test.txt` nu exista deja
- `fsutil file createnew filename.txt 1000` - creeaza fisierul `filename.txt` si ii aloca `1000` de bytes (pune spatii in fisier)

### Stergerea fisierelor
- `del file.txt` - sterge fisierul `file.txt`
- `del "nume cu spatii".txt` - sterge fisierul `nume cu spatii.txt`
- `del /f file.txt` - daca la stergere apar erori, `/f` face ca stergerea sa fie fortata

### Copierea fisierului de la o cale curenta la alta cale
- `copy test.txt secondfolderpath` 

### Copierea continutului de la calea_1 la calea_2
- `xcopy folderpath1 folderpath2`

### Copierea continutului folderului **gol** de la calea_1 la calea_2
- `xcopy calea_1 calea_2 /e /i`

### Mutarea unul folder de la calea_1 la calea_2
- `move folderpath1 folderpath2`

### Afisarea caii absolute
- `echo %CD%`

### Variabile de sistem

```console
set var=unText
echo %var%
```