# CRUD Angular
## Requisitos
- [Node JS - LTS](https://nodejs.org/pt-br/download/)
- Angular

## Após clonar o projeto
Abra o seu projeto no terminal:
>npm install

Executar o projeto:
>ng serve

## Extensões - Visual Studio
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
Estilos globais

### polyfills.ts
Suporte para navegadores mais antigos

### environments
Configuração de desenvolvimento e produção
