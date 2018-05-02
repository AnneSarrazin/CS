# Cours de C#

## Création de la structure  
### Création des projets indépendants  
`mkdir Isen.Cs && cd Isen.Cs`
`dotnet new sln`

#### Création du projet de type console
`mkdir Isen.Cs.ConsoleApp && cd Isen.Cs.ConsoleApp`
`dotnet new console

#### Création du projet de type librairie
`mkdir Isen.Cs.Library && cd Isen.Cs.Library`
`dotnet new classlib`

#### Création du prjet de tests unitaires
`mkdir Isen.Cs.Tests && cd Isen.Cs.Tests`
`dotnet new xunit`

### Référencement des projets
#### Ajouter au projet console/tests une référence vers le projet library 
` dotnet add reference ..\Isen.Cs.Library\Isen.Cs.Library.csproj`

### indiquer au sln la présence des 3 projets
`dotnet sln add Isen.Cs.Tests\Isen.Cs.Tests.csproj`

### Ménage
Effacer les fichiers .cs générer automatiquement à l'exception de celui du projet console.

### Build pour vérifier
3 étapes qui s'appellent entre elles lors d'un build:
 - `dotnet restore` : restaurer les packages "NuGet" distants
 - `dotnet build` : compiler les projets
 - `dotnet run` : executer
    * en console pour un projet console
    * lance un serveur web pour un projet web

### Initial commit
Créer un projet sur Github ou Gitlab.
Depuis la racine du projet :
`git init`
Trouver un .gitignore pour un projet .net Core (https://github.com/dotnet/core/blob/master/.gitignore)
`touch .gitignore`
Remplir avec le fichier exemple
`git add .`
`git commit -m "initial commit, project structure"`
`git remote add origin https://github.com/AnneSarrazin/CS.git`
`git push origin master`