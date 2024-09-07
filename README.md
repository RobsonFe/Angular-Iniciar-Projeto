# Guia para Iniciar um Projeto Angular: Clássico e Standalone

Este guia explica como iniciar um projeto Angular utilizando duas abordagens: o **Modelo Clássico com NgModules** (Angular 2+) e a nova abordagem de **Standalone Components** (Angular 17+).

## Descrição
O Angular passou por grandes mudanças ao longo das versões, e agora, com o Angular 17+, há uma nova forma de organizar os projetos utilizando **Standalone Components**, que simplificam a estrutura. Este documento aborda como iniciar projetos tanto no **modelo clássico** quanto na nova **abordagem standalone**.

## Pré-requisitos
Antes de começar, certifique-se de ter os seguintes itens instalados em seu ambiente:

- **Node.js** (versão 14 ou superior)
- **Angular CLI** (ferramenta de linha de comando do Angular)

---

## Documentação Oficial

- [Documentação Oficial do Angular 2+](https://v17.angular.io/)
- [Documentação Oficial do Angular 17+](https://angular.dev/)

---

### Instalando o Angular CLI
Se ainda não tiver a Angular CLI instalada, você pode fazer isso executando o seguinte comando:

```bash
npm install -g @angular/cli
```

---

## **Método Clássico (NgModules)**

O método clássico do Angular utiliza `NgModules` para organizar o projeto. Veja como iniciar um projeto dessa forma.

### 1. Criando o Projeto Clássico
Após instalar a CLI, crie um projeto Angular no modelo clássico (usando `NgModules`) com o seguinte comando:

```bash
ng new nome-do-projeto --no-standalone
```

O parâmetro `--no-standalone` garante que o projeto siga a arquitetura tradicional do Angular, onde componentes, diretivas e pipes são organizados em `NgModules`.

### 2. Criando Componentes no Modelo Clássico
Para criar novos componentes no modelo clássico, utilize o comando:

```bash
ng generate component nome-do-componente
```

Ou sua versão abreviada:

```bash
ng g c nome-do-componente
```

Os componentes criados desta forma serão registrados automaticamente no `AppModule` do projeto.

---

## **Método Standalone (Angular 17+)**

A partir do Angular 17, o uso de **Standalone Components** é o padrão. Essa nova abordagem elimina a necessidade de `NgModules` para organizar componentes, o que simplifica a estrutura do projeto.

### 1. Criando o Projeto com Standalone Components
Se estiver utilizando o Angular 17 ou superior, basta criar o projeto normalmente com o comando:

```bash
ng new nome-do-projeto
```

O projeto já será configurado para utilizar **Standalone Components** por padrão.

### 2. Criando Componentes Standalone
Caso esteja usando uma versão anterior ao Angular 17 e deseje criar um componente utilizando **Standalone Components**, adicione a flag `--standalone`:

```bash
ng generate component nome-do-componente --standalone
```

Ou sua versão abreviada:

```bash
ng g c nome-do-componente --standalone
```

Este comando cria um componente independente, que não requer associação a um `NgModule`.

---

# Bônus

## Principais Comandos do Angular CLI

Aqui estão alguns dos principais comandos que você usará com frequência ao desenvolver aplicações Angular:

- **Criar um novo projeto**:
  ```bash
  ng new nome-do-projeto
  ```
  
- **Servir a aplicação** (iniciar um servidor de desenvolvimento):
  ```bash
  ng serve
  ```
  
- **Servir a aplicação e abrir automaticamente no navegador**:
  ```bash
  ng s -o
  ```
  A aplicação estará disponível em [http://localhost:4200](http://localhost:4200) por padrão.
  
- **Gerar um novo componente**:
  - Modelo clássico (com `NgModule`):
    ```bash
    ng generate component nome-do-componente
    ```
    ou
    ```bash
    ng g c nome-do-componente
    ```
  - Modelo standalone (para versões anteriores ao Angular 17):
    ```bash
    ng generate component nome-do-componente --standalone
    ```
    ou
    ```bash
    ng g c nome-do-componente --standalone
    ```

- **Gerar um novo serviço**:
  ```bash
  ng generate service nome-do-servico
  ```
  ou
  ```bash
  ng g s nome-do-servico
  ```

- **Criar um módulo (modelo clássico)**:
  ```bash
  ng generate module nome-do-modulo
  ```
  ou
  ```bash
  ng g m nome-do-modulo
  ```

- **Executar testes unitários**:
  ```bash
  ng test
  ```

- **Construir a aplicação para produção**:
  ```bash
  ng build --prod
  ```

---

## Conclusão

- **Método Clássico**: Utiliza `NgModules` para organizar a aplicação. É ideal para quem está acostumado com as versões anteriores do Angular.
- **Método Standalone**: Simplifica a organização da aplicação, permitindo criar componentes independentes sem a necessidade de `NgModules`. Ideal para novos projetos no Angular 17+.

Escolha a abordagem que melhor se adapta ao seu projeto!

---
## Autor
[Robson Ferreira](https://github.com/RobsonFe)
