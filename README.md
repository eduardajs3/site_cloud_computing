# Galeria de Trabalhos - Cloud Computing

Exposicao dos trabalhos da turma FATEC 5o Semestre - Cloud Computing

---

## Como Adicionar Seu Trabalho

Siga o passo a passo abaixo para adicionar seu trabalho a galeria.

---

### Passo 1: Fazer Fork do Repositorio

O **fork** cria uma copia do repositorio na sua conta do GitHub.

1. Acesse o repositorio original no GitHub
2. Clique no botao **"Fork"** no canto superior direito da pagina
3. Selecione sua conta como destino do fork
4. Aguarde a copia ser criada

Apos o fork, voce tera uma copia do repositorio em `https://github.com/SEU_USUARIO/nome-do-repositorio`

---

### Passo 2: Clonar o Repositorio para sua Maquina

Abra o terminal e execute:

```bash
git clone https://github.com/SEU_USUARIO/nome-do-repositorio.git
```

Substitua `SEU_USUARIO` pelo seu usuario do GitHub e `nome-do-repositorio` pelo nome do repositorio.

Entre na pasta do projeto:

```bash
cd nome-do-repositorio
```

---

### Passo 3: Criar seu Arquivo HTML

#### Se quiser pode utilizar um dos Templates Disponiveis

Temos 3 templates diferentes para voce escolher. Acesse a galeria e clique no botao de templates (icone de layout) ao lado do botao de tema para visualizar cada um.

| Template | Descricao |
|----------|-----------|
| **Cards Coloridos** | Grid 3x3 com cards em gradiente colorido. Visual vibrante e moderno com fundo escuro. |
| **Timeline** | Layout vertical com linha do tempo. Cards alternando esquerda e direita com visual elegante. |
| **Minimalista** | Design clean com fundo claro. Cards com bordas sutis e destaque em azul no hover. |

Os templates estao na pasta `templates/`:
- `templates/template-cards.html`
- `templates/template-timeline.html`
- `templates/template-minimal.html`

1. Acesse a pasta `templates/` e escolha o template que mais gostar;

2. Copie o template escolhido para a pasta `trabalhos/` e renomeie

```bash
3. Customize o template com seu conteúdo e estilos de preferência
```

**Padrao de nomenclatura:** use seu primeiro nome em minusculo, sem acentos ou espacos.
- Exemplo: `lucas.html`, `maria.html`, `joao.html`
- Se houver nomes repetidos, use nome + inicial do sobrenome: `lucasS.html`

3. Abra o arquivo `trabalhos/seuNome.html` em um editor de texto (VS Code por exemplo)

4. Edite o conteudo com as informacoes do seu trabalho:
   - Altere o `<title>` com seu nome
   - Preencha os 9 servicos AWS
   - Adicione seu nome completo no header

**Dica:** Consulte o arquivo `trabalhos/lucasF.html` como exemplo de referencia.

---

### Estilizando seu Trabalho com Tailwind CSS

O template utiliza **Tailwind CSS** para estilizacao, ja incluido via CDN.

Tailwind e um framework CSS utilitario onde voce aplica classes diretamente nos elementos HTML em vez de escrever CSS tradicional.

**Documentacao oficial:** [https://tailwindcss.com/docs](https://tailwindcss.com/docs)

---

### Passo 4: Registrar seu Trabalho no index.html

1. Abra o arquivo `index.html` na raiz do projeto

2. Localize o array `alunos` no inicio do bloco `<script>`, linha 227:

```javascript
const alunos = [
    { id: 'lucasF', nome: 'Lucas Ferreira Nogueira' },
    // ... outros alunos
];
```

3. Adicione uma nova linha com seus dados:

```javascript
const alunos = [
    { id: 'lucasF', nome: 'Lucas Ferreira Nogueira' },
    // ... outros alunos
    { id: 'seuNome', nome: 'Seu Nome Completo' },  // <-- Adicione aqui
];
```

**Importante:**
- O `id` deve ser **exatamente igual** ao nome do seu arquivo (sem o `.html`)
- O `nome` sera exibido no card da galeria

**Exemplo:**
Se seu arquivo e `lucas.html`, adicione:
```javascript
{ id: 'lucas', nome: 'Lucas Ferreira Nogueira' },
```

---

### Passo 5: Testar Localmente

Antes de enviar, teste se tudo esta funcionando:

1. Abra o arquivo `index.html` no navegador
2. Verifique se seu card aparece na galeria
3. Clique no seu card e confirme se seu trabalho abre corretamente

---

### Passo 6: Fazer Commit e Push

Salve suas alteracoes no Git:

```bash
git add .
git commit -m "Adiciona trabalho de [Seu Nome]"
git push origin main
```

---

### Passo 7: Abrir Pull Request

O **Pull Request (PR)** solicita que suas alteracoes sejam incorporadas ao repositorio original.

1. Acesse **seu fork** no GitHub (`https://github.com/SEU_USUARIO/nome-do-repositorio`)

2. Voce vera uma mensagem indicando que seu branch esta a frente do original. Clique em **"Contribute"** e depois **"Open pull request"**

   *Ou acesse a aba "Pull requests" e clique em "New pull request"*

3. Verifique se esta comparando:
   - **base repository:** repositorio original (do professor)
   - **head repository:** seu fork
   - **base:** main ← **compare:** main

4. Clique em **"Create pull request"**

5. Preencha o titulo e descricao:
   - **Titulo:** `Adiciona trabalho de [Seu Nome]`
   - **Descricao:** Breve resumo do seu trabalho

6. Clique em **"Create pull request"** para finalizar

Aguarde a revisao e aprovacao do professor.

---

## Estrutura do Projeto

```
atividade_site/
├── index.html              <- Pagina principal (galeria)
├── README.md               <- Este arquivo
├── templates/              <- Templates disponiveis
│   ├── template-cards.html     <- Grid colorido
│   ├── template-timeline.html  <- Linha do tempo
│   └── template-minimal.html   <- Minimalista
└── trabalhos/
    ├── template.html       <- Template antigo (use os da pasta templates/)
    ├── lucasF.html         <- Exemplo de referencia
    └── seuNome.html        <- Seu trabalho (criar)
```

---

## Checklist antes de enviar o PR

- [ ] Criei meu arquivo em `trabalhos/meuNome.html`
- [ ] Editei o conteudo com as informacoes do meu trabalho
- [ ] Adicionei minha entrada no array `alunos` em `index.html`
- [ ] Testei localmente e meu card aparece na galeria
- [ ] Meu trabalho abre corretamente ao clicar no card
- [ ] Fiz commit com mensagem descritiva
- [ ] Abri o Pull Request no repositorio original

---

## Duvida imagens

**P: Posso adicionar imagens ao meu trabalho?**
R: Sim, crie uma pasta com seu nome dentro de `trabalhos/` (ex: `trabalhos/lucas/`) e coloque suas imagens la. Referencie no HTML com caminho relativo.

