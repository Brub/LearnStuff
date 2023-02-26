# .gitignore

Vaak zul je een klasse bestanden hebben waarvan je niet wilt dat Git deze automatisch toevoegt of zelfs maar als untracked toont. Dit zijn doorgaans automatisch gegenereerde bestanden zoals logbestanden of bestanden die geproduceerd worden door je bouwsysteem.  
In die gevallen kun je een bestand genaamd `.gitignore` maken, waarin patronen staan die die bestanden passen.  
Een `.gitignore` bestand aanmaken voordat je gaat beginnen is over het algemeen een goed idee, zodat je niet per ongeluk bestanden commit die je echt niet in je Git repository wilt hebben.  

## Regels die van toepassing zijn met het .gitignore bestand
- lege lijnen worden genegeerd
- lijnen die starten met een `#` worden genegeerd (info: zijn commentaar lijnen)  
- `*` komt overeen met nul of meer karakters
- `**`  twee asterisken gebruiken om geneste directories aan te geven (volgens het voorbeeld: komt overeen met a/z, a/b/z, a/b/c/z en zo verder)
- `[abc]` komt overeen met ieder karakter dat tussen de blokhaken staat (in dit geval a, b of c)
- `[0-9]` komen overeen met ieder karakter dat tussen die karakters zit (in dit geval 0 tot en met 9)  
- `?` komt overeen met een enkel karakter
- `/` om een patroon te laten starten of eindigen

## Voorbeeld van een .gitignore file

```
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# ignore all .c and .h files
*.[ch]

# ignore all files ending with a ~
*~

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in any directory named build
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
```
## Toon de ignored bestanden
Gebruik het commando `git status --ignored` om deze bestanden te tonen.


## Extra info

[https://www.atlassian.com/git/tutorials/saving-changes/gitignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)  
[https://www.w3schools.com/git/git_ignore.asp?remote=github](https://www.w3schools.com/git/git_ignore.asp?remote=github)
