# 📱 Calculadora de IMC Multiplataforma

Este repositório contém uma aplicação funcional de Calculadora de IMC construída com o framework **Flutter**. O projeto foi desenvolvido com foco prático em engenharia de software e desenvolvimento multiplataforma (cross-platform), garantindo que o código lógico em Dart permaneça intacto enquanto o framework gerencia as execuções nativas.

O grande diferencial deste projeto é a sua infraestrutura: a aplicação foi codificada em nuvem e conta com uma esteira de Integração e Entrega Contínuas (CI/CD) totalmente automatizada.

## 🚀 Tecnologias Utilizadas

* **Front-end:** Flutter & Dart
* [cite_start]**Ambiente de Desenvolvimento:** GitHub Codespaces
* **Isolamento de Build:** Docker (Ubuntu 22.04)
* **CI/CD:** GitHub Actions
* **Hospedagem Web:** GitHub Pages

## 🛠️ Arquitetura e Fluxo de Desenvolvimento

### 1. Desenvolvimento em Nuvem (GitHub Codespaces)

Para otimizar recursos locais, o desenvolvimento ocorreu no GitHub Codespaces. [cite_start]Como a imagem padrão do Codespaces não inclui o SDK do Flutter nativamente, o ambiente foi configurado via terminal clonando o canal estável do framework (`git clone -b stable https://github.com/flutter/flutter.git ~/flutter`) e mapeando o executável nas variáveis de ambiente (`export PATH="$PATH:$HOME/flutter/bin"`). Após essa etapa, as plataformas foram geradas dinamicamente com o comando `flutter create --platforms web, android`.

### 2. Automação com GitHub Actions (CI/CD)

O repositório possui dois fluxos independentes de execução paralela configurados na pasta `.github/workflows/`:

* **Deploy Web Automático:** Uma pipeline compila os arquivos web e realiza o deploy automaticamente no GitHub Pages sempre que um push é feito na branch `main`.
* **Compilação Android via Docker:** Para garantir um processo de build idêntico em qualquer servidor, utilizamos o Docker. A Action constrói a imagem Docker, extrai o binário gerado (APK) internamente e o disponibiliza para download direto como artefato no painel do GitHub.

## ⚙️ Como visualizar o projeto

### Versão Web

Acesse a aplicação rodando diretamente no seu navegador através do GitHub Pages:
🔗 **[Insira o link do seu GitHub Pages aqui, ex: https://flprocha236.github.io/calculadoraflutter/]**

### Versão Android (APK)

1. Acesse a aba **Actions** deste repositório.
2. Clique na última execução com sucesso do fluxo `Flutter_Build_Action`.
3. Desça até o final da página e, na seção **Artifacts**, faça o download do `app-final-build` para instalar o APK no seu dispositivo Android.

## 👨‍💻 Sincronização e Desenvolvimento Local

Caso queira clonar este projeto e rodar localmente após o uso do Codespaces, utilize o GitHub Desktop ou a CLI para realizar o `fetch` e `pull` das atualizações. Isso garantirá que toda a árvore de arquivos, incluindo as pastas nativas geradas em nuvem, sejam baixadas corretamente.

---

*Projeto desenvolvido para a disciplina de Desenvolvimento Multiplataforma - FATEC Araras.* 
