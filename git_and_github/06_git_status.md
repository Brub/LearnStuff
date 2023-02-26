# git status

Via dit commando kan je de status van je bestanden controleren.

```
git status
```  
Nu worden er 2 soorten info afgebeeld:  
* de naam van de branch op dewelke je aan het werken bent
* de status van de branch, dit wordt uitgelegd in de volgende onderdelen

## nothing to commit, working tree clean
```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```

Dit betekent dat je een schone werkdirectory hebt; met andere woorden er zijn geen tracked bestanden die gewijzigd zijn.


## Untracked files
```
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

    README

nothing added to commit but untracked files present (use "git add" to track)
```
Untracked betekent eigenlijk dat Git een bestand ziet dat je niet in de vorige snapshot (commit) had; Git zal het niet aan je commit snapshots toevoegen totdat jij dit expliciet aangeeft. De reden hiervoor is dat je niet per ongeluk gegenereerde binaire bestanden toevoegt, of andere bestanden die je niet had willen toevoegen.  
Om een nieuw bestand te beginnen te tracken, gebruik je het commando `git add`.


## Changes to be committed
Deze meldinge betekend dat git nog geen info heeft over de veranderingen van de afgebeelde bestanden.

Als je aan git wil vertellen wat de varanderingen zijn moet je het volgende commando gebruiken

```
git commit -m "de uitleg wat er veranderd is"
```


