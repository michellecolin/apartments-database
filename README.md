# 🏠 Apê Finder

Aplicação para comparar apartamentos durante a busca pelo apê ideal.

## Setup

### 1. Criar o repositório

Crie um repositório **público** no GitHub (ex: `apartamentos`).

### 2. Gerar um token fine-grained

1. Vá em [GitHub Settings → Developer Settings → Fine-grained tokens](https://github.com/settings/tokens?type=beta)
2. Clique em **"Generate new token"**
3. Dê um nome (ex: "Apê Finder")
4. Em **Repository access**, selecione **"Only select repositories"** e escolha o repositório criado
5. Em **Permissions → Repository permissions**, dê permissão de **Read and write** para **Contents**
6. Gere o token e copie

### 3. Configurar o app

Abra o arquivo `index.html` e edite as linhas no topo do JavaScript:

```javascript
const GITHUB_TOKEN = 'github_pat_SEU_TOKEN_AQUI';
const GITHUB_REPO = 'seu-usuario/apartamentos';
```

### 4. Fazer o deploy

1. Faça commit dos arquivos (`index.html`, `data.json`, `README.md`) no repositório
2. Vá em **Settings → Pages**
3. Em **Source**, selecione **Deploy from a branch**
4. Escolha a branch `main` e pasta `/ (root)`
5. Aguarde alguns minutos e acesse `https://seu-usuario.github.io/apartamentos`

## Funcionalidades

- ✅ Cadastro de apartamentos com todas as informações
- ✅ Fotos via URL
- ✅ Sistema de avaliação com notas (0-5) e comentários
- ✅ Nota geral calculada automaticamente
- ✅ Filtros por status, quartos, vagas
- ✅ Ordenação por preço, área, nota, condomínio
- ✅ Busca por endereço
- ✅ Comparação lado a lado (até 3 aptos)
- ✅ Gestão de status: Novo → Visitado → Favorito / Rejeitado
- ✅ Persistência via GitHub API (data.json)
- ✅ Zero backend, zero banco de dados

## Segurança

O token fica exposto no código-fonte. Como o token tem permissão **apenas** neste repositório e os dados são apenas apartamentos, o risco é mínimo. O pior cenário é alguém editar seu `data.json`.
