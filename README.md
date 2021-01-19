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

17)
