# git status

Via dit commando kan je de status bekijken van het project.

```
git status
```  
De info die je nu terug krijgt zullen we in de volgende secties bespreken.

## Untracked files
Deze melding wordt getoond als je nieuwe bestanden hebt toegevoegd aan het project maar die nog niet beheerd worden door git.
Als je deze wil toevoegen om beheerd te worden kanje het volgende commando gebruiken

```
git add filename.extention
```
als je alle 'Untracked files' wil toevoegen kan je het volgende commando gebruiken
```
git add .
```

## Changes to be committed
Deze meldinge betekend dat git nog geen info heeft over de veranderingen van de afgebeelde bestanden.

Als je aan git wil vertellen wat de varanderingen zijn moet je het volgende commando gebruiken

```
git commit -m "de uitleg wat er veranderd is"
```

## nothing to commit, working tree clean
Dit wil zeggen dat je lokaal project geen wijzigingen heeft.
