# Dio Board Java

Este é um projeto de linha de comando para gerenciar quadros no estilo Kanban. Ele permite que os usuários criem, selecionem e excluam quadros. Ao criar um quadro, os usuários podem definir colunas personalizadas, além das colunas padrão "inicial", "final" e "cancelar".

## Tecnologias Utilizadas

* **Java:** Linguagem de programação principal.
* **Gradle:** Ferramenta de automação de compilação.
* **Liquibase:** Para controle de versão do esquema do banco de dados.
* **MySQL:** O projeto está configurado para se conectar a um banco de dados MySQL.
* **Lombok:** Para reduzir o código boilerplate.

## Como Rodar o Projeto

1. **Pré-requisitos:**
   - JDK (Java Development Kit) instalado.
   - Gradle instalado.
   - Um servidor de banco de dados MySQL em execução.

2. **Configuração do Banco de Dados:**
   - Crie um banco de dados no seu servidor MySQL.
   - As configurações de conexão com o banco de dados (URL, usuário e senha) precisam ser ajustadas nos arquivos de configuração do Liquibase (não inclusos neste projeto base, mas normalmente `liquibase.properties` ou similar).

3. **Executando as Migrações:**
   - O projeto está configurado para usar o Liquibase. Para aplicar as migrações de banco de dados, você pode executar as tarefas do Gradle relacionadas ao Liquibase. A tarefa principal para aplicar as changesets é `update`.
   ```bash
   gradle update
   ```

4. **Executando a Aplicação:**
   - Para construir o projeto, execute:
   ```bash
   gradle build
   ```
   - Para rodar a aplicação (supondo que haja uma classe principal configurada no `build.gradle.kts`), você pode usar a tarefa `run`.
   ```bash
   gradle run
   ```
