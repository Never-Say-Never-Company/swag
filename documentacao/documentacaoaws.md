# Manual de Configuração: Credenciais AWS para Ambiente de Desenvolvimento

## 1. Objetivo

Este manual descreve o processo padrão para desenvolvedores configurarem suas credenciais da AWS no ambiente de desenvolvimento local. Isso garante que o **AWS CLI**, o **Docker** e bibliotecas como **boto3** (usada pelo Python) possam se autenticar corretamente com a AWS.

## 2. Passo a Passo da Configuração

### Etapa 1: Recebimento das Credenciais

O Administrador da conta AWS (Admin) será responsável por gerar um par de chaves de acesso (Access Key) no IAM para cada desenvolvedor.

Você receberá de forma segura dois valores essenciais:
* `AWS Access Key ID`
* `AWS Secret Access Key`

### Etapa 2: Instalação do AWS CLI

O AWS Command Line Interface (CLI) é a ferramenta usada para configurar seu perfil de credenciais local.

Se você ainda não o possui, faça o download e instale a partir do link oficial:
[https://aws.amazon.com/cli/](https://aws.amazon.com/cli/)

### Etapa 3: Configuração do Perfil Local

Abra seu terminal (Prompt de Comando, PowerShell, Terminal, etc.) e execute o seguinte comando:

```bash
aws configure
```
O CLI solicitará quatro informações. Preencha os campos exatamente como abaixo, colando os valores que você recebeu na Etapa 1:

1. **AWS Access Key ID [None]:** `(Cole o valor AWS Access Key ID recebido)`
2. **AWS Secret Access Key [None]:** `(Cole o valor AWS Secret Access Key recebido)`
3. **Default region name [None]:** `sa-east-1`
4. **Default output format [None]:** `(Pressione Enter para deixar em branco)`

### Etapa 4: Verificação (Automático)

Ao concluir o `aws configure`, o AWS CLI cria (ou atualiza) automaticamente os arquivos necessários no diretório `.aws` do seu usuário.

- **Localização:**
    - **Windows:** `C:\Users\SEU_USUARIO\.aws\credentials`
    - **Linux/macOS:** `~/.aws/credentials`

Este arquivo `credentials` será lido automaticamente por outras ferramentas (como `boto3` e Docker), eliminando a necessidade de editar arquivos manualmente ou expor chaves em arquivos `.env`.

### Etapa 5: Integração com Docker

Para que seus contêineres Docker possam usar as credenciais configuradas na Etapa 3, o diretório `.aws` do seu computador (host) precisa ser montado como um volume *read-only* (somente leitura) dentro do contêiner.

No docker-compose.yml, use:
```

    volumes:
      - .:/code    # Mapeia o código-fonte do projeto
      - .:/rootc.aws:ro
      
```

## 3. Contatos

Para dúvidas ou pedido de novas chaves, entre em contato com o Administrador da conta AWS (Admin).