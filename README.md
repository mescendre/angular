![Angular Logo](https://github.com/vercel/vercel/blob/master/packages/frameworks/logos/angular.svg)

# Angular Example

This directory is a brief example of an [Angular](https://angular.io/) app that can be deployed with Vercel and zero configuration.

## Deploy Your Own

Deploy your own Angular project with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/vercel/vercel/tree/master/examples/angular)

_Live Example: https://angular.now-examples.now.sh_

### How We Created This Example

To get started with Angular, you can use the [Angular CLI](https://cli.angular.io/) to initialize the project:

```shell
$ ng new
```


4)
npm i -g vercel

5)
C:\Users\Antoine>vercel init
Vercel CLI 21.1.0
> Select example: angular
> Success! Initialized "angular" example in ~\angular.
- To deploy, `cd angular` and run `vercel`.

6)
C:\Users\Antoine\Desktop\EI5\Voisin>vercel deploy angular
Vercel CLI 21.1.0
? Set up and deploy “~\Desktop\EI5\Voisin\angular”? [Y/n] y
? Which scope do you want to deploy to? mescendre
? Found project “mescendre/angular”. Link to it? [Y/n] y
�  Linked to mescendre/angular (created .vercel and added it to .gitignore)
�  Inspect: https://vercel.com/mescendre/angular/6yn6kwzos [1s]
✅  Production: https://angular-beryl-tau.vercel.app [copied to clipboard] [1m]
�  Deployed to production. Run `vercel --prod` to overwrite later (https://vercel.link/2F).
�  To change the domain or build command, go to https://vercel.com/mescendre/angular/settings

7) vercel ls angular
> Deployments under mescendre [529ms]
Vercel CLI 21.1.0
  project    latest deployment               state    age    username
  angular    angular-6yn6kwzos.vercel.app    READY    7m     mescendre
  
8) vercel logs https://angular-beryl-tau.vercel.app/

9) vercel inspect angular-6yn6kwzos.vercel.app
renvois l'ID, le nom, l'état et l'url de l'appli, montre aussi l'arborescence du projet 

10)permet de linker différents processus au code
permet d'injecter des valeurs que vous ne souhaitez pas placer directement dans votre code source
et de modifier son comportement en fonction de l'environnement dans lequel il s'exécute.

11)
C:\Users\Antoine\Desktop\EI5\Voisin>vercel env add plain EnvPlain production
Vercel CLI 21.1.0
? What’s the value of EnvPlain?
✅  Added Environment Variable EnvPlain to Project test [593ms]

12)
C:\Users\Antoine\Desktop\EI5\Voisin>vercel env ls production
Vercel CLI 21.1.0
> Environment Variables found in Project test [517ms]

 name        value    environments        created
 EnvPlain             Production          2m ago
 
13)
les variables secret sont chiffrées et constituent un moyen sécurisé de stocker et de partager des informations sensibles entre les déploiements.

14) fait avec vercelWeb

15)
C:\Users\Antoine\Desktop\EI5\Voisin>vercel secrets add new_secret2 MonSecret
Vercel CLI 21.1.0
Success! Secret new_secret2 added under mescendre [654ms]

16)Vercel met à disposition les 3 environements suivants : <production | preview | development>

Production
When selected, the Environment Variable will be applied to your next Production Deployment.
To create a Production Deployment, push a commit to the Production Branch or run vercel --prod.

Preview
The Environment Variable is applied to your next Preview Deployment.
 Preview Deployments are created when you push to a branch (for example, my-new-feature) or run vercel.
 
Development
The Environment Variable is for use when running your project locally, with vercel dev or your preferred development command.
To download Development Environment Variables, run vercel env pull.

17) fait depuis github

18) Renseignez l'adresse automatiquement générée par Vercel : https://angular-git-main.mescendre.vercel.app/

19) Au moment du pull request, c'est l'environement preview qui est impacté, Vercel met en commun les deux branches de manière à donner un aperçu de al combinaison des modifications présentes sur les deux branches.

20) Au moment de merge, c'est l'environement de produciton qui est impacté, vercel  se replace dans l'environement de production pour montrer le résultat actuel de l'application

21) l'environnement de production correspond à la branche principale main), l'intérêt de faire des pull request permet de garder l'affichage du projet à jour sans forcément impacter l'environnement de production
pour le workflow, la feature passe de développement à visualisation, et si tout est bon à production.

22) 
permet de déployer des fonctions sans serveur, écrits avec des langages backend qui acceptent une requête HTTP et fournissent une réponse.
Cette utilisation permet d'implémenter des fonctions spécifiques sans serveur (comme gérer l'authentification d'utilisateurs, les formulaires, des requêtes BDD...)

23)
