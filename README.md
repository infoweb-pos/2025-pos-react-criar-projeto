# Atividade - React - Criar um projeto novo

## Informações gerais

- **Público alvo**: alunos da disciplina de POS (Programação Orientada a Serviços) do curso de Infoweb (Técnico Integrado em Informática para Internet) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central)
- **Professor**: [L A Minora](https://github.com/leonardo-minora/)
- **Aluno**: FIXME
- **Obetivos**
  1. Aprender a criar novo projeto de um aplicativo react
  2. Aprender a criar (configurar) uma pasta (diretório) como respositório git
  3. Aprender a conectar um repositório git local a um remoto  



## Passos da atividade

1. Criar um projeto react de um aplicativo web
2. Instalar bibliotecas e executar aplicativo web
3. Apagar arquivo `README.md`
4. Modificar arquivo `.gitignore`
5. Modificar arquivo `src/app/layout.tsx`
6. Modificar arquivo `src/app/page.tsx`
7. Inicializar a pasta do projeto como repositório git
8. Guardar localmente a primeira versão do projeto
9. Conectar ao repositório remoto
10. Trazer as atualizações do repositório remoto para repositório local
11. Modificar arquivo `README.md`
12. Guardar localmente a segunda versão do projeto
13. Publicar as modificações locais no repositório remoto



### 1. Criar um projeto react de um aplicativo web

O comando para criar um novo projeto é `npx create-next-app@latest react-01-criar-projeto --disable-git --skip-install --yes`, conforme mostrado no terminal abaixo.

Descrevendo o comando:
- `npx` : software instalado junto com o node e npm que tem a função de executar script publicados em https://www.npmjs.com/
- `create-next-app` : script responsável por criar uma pasta e colocar arquivos para um projeto react/next
- `@latest` : verifica e pega a última versão publicada em https://www.npmjs.com/
- `react-01-criar-projeto` : nome do projeto e da pasta que será criada
- `--disable-git` : a pasta do projeto não será inicializada como repositório git
- `--skip-install` : pula o processo de pegar as bibliotecas em https://www.npmjs.com/
- `--yes` : responde sim para todos as perguntas

```shell
$ npx create-next-app@latest react-01-criar-projeto --disable-git --skip-install --yes

Need to install the following packages:
create-next-app@15.2.4
Ok to proceed? (y) y

Creating a new Next.js app in /home/minora/minora/2025/react-01-criar-projeto.

Using npm.

Initializing project with template: app-tw 

Skipping git initialization.

Success! Created react-01-criar-projeto at /home/minora/minora/2025/react-01-criar-projeto

$ 
```



### 2. Instalar bibliotecas e executar aplicativo web

Para instalar as bibliotecas do projeto, será necessário estar dentro da pasta do projeto.
Usar o comando `cd react-01-criar-projeto` para aceder a pasta do projeto, conforme terminal abaixo.
Curiosidade, `cd` é acrônimo para _change directory_.

```shell
$ cd react-01-criar-projeto

[minora@fedora react-01-criar-projeto] $ 
```

Estando dentro da pasta do projeto, agora você pode usar comandos para executar, criar distribuição, adicionar/remover/atualizar versão de bibliotecas, etc.
Para o momento, executar o comando `npm i` para pegar as bibliotecas em https://www.npmjs.com/ e colocar na pasta `node_modules`.
A lista de bibliotecas necessárias ao projeto esta disposta no arquivo `package.json`.
O terminal abaixo mostra um exemplo de execução do comando.

```shell
[minora@fedora react-01-criar-projeto] $ npm i

added 317 packages, and audited 318 packages in 17s

131 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

[minora@fedora react-01-criar-projeto] $ 
```

O parâmetro `i` tem vários sinônimos que na versão que foi feito esse tutorial, permitia os seguintes: add, i, in, ins, inst, insta, instal, isnt, isnta, isntal, isntall.
Para detalhes sobre este parâmetro, pode executar `npm i --help`.

Com as bibliotecas instaladas, agora é hora de executar o aplicativo web com o comando `npm run dev`, como mostrado no terminal abaixo.

```shell
[minora@fedora react-01-criar-projeto] $ npm run dev

> react-01-criar-projeto@0.1.0 dev
> next dev --turbopack

   ▲ Next.js 15.2.4 (Turbopack)
   - Local:        http://localhost:3000
   - Network:      http://192.168.68.119:3000

 ✓ Starting...
 ✓ Ready in 1534ms


```

Para finalizar o aplicativo, pressione `CTRL+C` no terminal onde ele esta em execução.
Não finalize agora, antes acesse o endereço http://localhost:3000 e veja sua aplicação recém criada.
Mantenha assim, para verificar suas futuras modificações foram aplicadas corretamente.



### 3. Apagar arquivo `README.md`

```shell
[minora@fedora react-01-criar-projeto] $ rm README.md

```

### 4. Modificar arquivo `.gitignore`

Adicionar os arquivos de _lock_ de projetos javascript no arquivo `.gitignore`.
O arquivo final deve ficar conforme o arquivo abaixo.

```
# See https://help.github.com/articles/ignoring-files/ for more about ignoring files.

# lock files
package-lock.json
pnpm-lock.yaml
yarn.lock

# dependencies
/node_modules
/.pnp
.pnp.*
.yarn/*
!.yarn/patches
!.yarn/plugins
!.yarn/releases
!.yarn/versions

# testing
/coverage

# next.js
/.next/
/out/

# production
/build

# misc
.DS_Store
*.pem

# debug
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.pnpm-debug.log*

# env files (can opt-in for committing if needed)
.env*

# vercel
.vercel

# typescript
*.tsbuildinfo
next-env.d.ts
```

### 5. Modificar arquivo `src/app/layout.tsx`

### 6. Modificar arquivo `src/app/page.tsx`

### 7. Inicializar a pasta do projeto como repositório git

```shell
[minora@fedora react-01-criar-projeto] $ git init

```

```shell
[minora@fedora react-01-criar-projeto] $ git config user.email "leonardo.minora@gmail.com"

```


```shell
[minora@fedora react-01-criar-projeto] $ git git config user.name "L A Minora"

```


### 8. Guardar localmente a primeira versão do projeto

```shell
[minora@fedora react-01-criar-projeto] $ git add status

[minora@fedora react-01-criar-projeto] $ git add .

[minora@fedora react-01-criar-projeto] $ git commit -m "adicionado projeto novo conforme atividade da disciplina"

```

### 9. Conectar ao repositório remoto

Fazer um fork do repositório da atividade [criar projeto react](https://github.com/infoweb-pos/2025-pos-react-criar-projeto) para sua conta pessoal do [github](https://github.com/).

Após o fork, pegar a URL do repositório da sua conta e executar o comando `git remote add origin URL`, conforme terminal abaixo.
Lembrar de substituir `URL` pela URL de fato do seu repositório.


Para verficar se funcionou, executar o comando `git remote -v`.
O terminal aparecerá informações da _tag_ `origin` como mostrado no terminal abaixo na execução do 2o comando.

```shell
[minora@fedora react-01-criar-projeto] $ git remote add origin URL

[minora@fedora react-01-criar-projeto] $ git remote -v
origin	https://github.com/leonardo-minora/2025-pos-react-criar-projeto.git (fetch)
origin	https://github.com/leonardo-minora/2025-pos-react-criar-projeto.git (push)

[minora@fedora react-01-criar-projeto] $ 
```

### 10. Trazer as atualizações do repositório remoto para repositório local

```shell
[minora@fedora react-01-criar-projeto] $ git pull origin main

```

### 11. Modificar arquivo `README.md`

Procurar por FIXME e colocar o nome do aluno.
Pode colocar como hiperlink para sua conta do github, como feito no nome do professor.

### 12. Guardar localmente a segunda versão do projeto

```shell
[minora@fedora react-01-criar-projeto] $ git status


[minora@fedora react-01-criar-projeto] $ git add .

[minora@fedora react-01-criar-projeto] $ git commit -m "adicionado nome do aluno em README"

```

### 13. Publicar as modificações locais no repositório remoto

```shell
[minora@fedora react-01-criar-projeto] $ git push origin main

```
