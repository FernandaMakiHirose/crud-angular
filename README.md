# CRUD Angular
## Requisitos
- [Node JS - LTS](https://nodejs.org/pt-br/download/)
- Angular

## Após clonar o projeto
Abra o seu projeto no terminal:
>npm install

Executar o projeto:
>ng serve

## Organizar os imports do app.module.ts
1. No Visual Studio Code > View > Command Pallete > TS Hero: Organize imports (sort and remove unused)
1.2 Irá adicionar boas práticas e deixa os imports em ordem alfabética

## Angular Material
- [Toolbar](https://v7.material.angular.io/components/toolbar/overview)
1. Em "API" copiei o código e colei/importei no `app.module.ts` para fazer o uso do Toolbar
2. O código foi adicionado no arquivo `app.component.html`

- [Lazy Loading](https://angular.io/guide/lazy-loading-ngmodules)
- [Paleta de cores](https://material.io/design/color/the-color-system.html#tools-for-picking-colors)
- [Criar paleta de cores personalizada](https://material.angular.io/guide/theming)

## Extensões - Visual Studio Code
- Angular Extension Pack - Loiane Groner

## Comandos
Verificar a existência do Node JS:
>node -v

Instalar o Angular:
>npm install -g @angular/cli

Verificar a versão do Angular:
>ng --version

Criação do projeto Angular:
>ng new crud-angular

1. Would you like to add Angular routing? Yes
2. SCSS

Instalar o Angular Material:
>ng add @angular/material

1. Would you like to proceed? Yes
2. Indigo/Pink
3. Set up global Angular Material typography styles? Yes
4. Set up browser animations for Angular Material? Yes

Criar o módulo e roteamento:
>ng g m nomedomodulo --routing

Criar o módulo sem o roteamento:
>ng g m nomedomodulo

Criar um componente dentro de um módulo:
>ng g c nomedomodulo/nomedocomponente

## Entendendo o código
### package.json
Todas as dependências e bibliotecas usadas estão no arquivo. As bibliotecas estão em `devDependencies`, elas são usadas apenas no momento de desenvolvimento do projeto 

### angular.json
É uma forma de definir inicializar as variáveis
```
"strict": true
```

Tamanhos máximos que arquivos JavaScript podem ter
```
"budgets": []
```

### .browserslistrc 
São os navegadores que vão conseguir carregar o projeto

### test.ts 
Local para utilizar o Jasmine e o Karma

### styles.scss
Estilos globais, como paleta de cor 
```
@import '@angular/material/theming';
@include mat-core();

$custom-app-primary: mat-palette($mat-blue);
$custom-app-secondary: mat-palette($mat-indigo, A200, A400, 700);
$custom-app-warn: mat-palette($mat-red);

$custom-theme: mat-light-theme($custom-app-primary, $custom-app-secondary,  $custom-app-warn);

@include angular-material-theme($custom-theme);
```

### polyfills.ts
Suporte para navegadores mais antigos

### environments
Configuração de desenvolvimento e produção

### componente-routing.module.ts
Rotas do componente

### app-routing.module.ts
Rotas global

Significa que a rota irá carregar sem considerar a porta localhost:
```
pathMatch: 'full'
```

Para adicionar um módulo filho, usamos o Lazy Loading:
```
const routes: Routes = [
  {
    path: 'nomedocaminhoquevocequercriar',
    loadChildren: () => import('./nomedomodulo/nomedomodulo.module').then(m => m.NomeDoModulo)
  }
];
```

### app.component.html
Faz o redirecionamento da rota do módulo:
```
<router-outlet></router-outlet>
```
