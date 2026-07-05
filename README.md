# Formulário de Treino → PDF

Página única (`index.html`) com um formulário de anamnese para ciclo de treino de corrida, que gera um PDF formatado no próprio navegador — sem backend e sem envio de dados a nenhum servidor.

## Como funciona

1. O atleta preenche o formulário, organizado em seções: Prova, Objetivo, Histórico, Rotina, Saúde, Fortalecimento, Ritmo e Dados pessoais.
2. Ao clicar em **"Gerar PDF"**, o JavaScript lê todos os campos preenchidos (texto, seleção única em pílulas/radio, seleção múltipla em checkboxes) e monta um documento PDF com [jsPDF](https://github.com/parallax/jsPDF), seção por seção, com títulos e emojis.
3. O PDF é baixado automaticamente com o nome do arquivo derivado do nome da prova informado (ex.: `formulario_meia_maratona_da_cidade.pdf`).
4. Campos não preenchidos aparecem no PDF como `—`. Não há validação obrigatória: o formulário pode ser enviado parcialmente preenchido.
5. O resultado é entregue ao coach como um único PDF organizado, substituindo o preenchimento manual de uma anamnese em texto livre.

## Stack

- HTML + CSS + JavaScript puro, sem framework e sem build step.
- Fonte **Inter** via Google Fonts.
- Geração de PDF client-side com **jsPDF** (carregado via CDN).
- Sem dependência de backend: tudo roda no navegador, compatível com GitHub Pages ou uso local.

## Estrutura do projeto

```
index.html    # Formulário (HTML + CSS) e lógica de geração do PDF (JS)
```

## Rodando localmente

Não há dependências nem build. Basta abrir o `index.html` diretamente no navegador ou servir a pasta com qualquer servidor estático:

```bash
npx serve .
```

## Deploy

Compatível com publicação estática direta no GitHub Pages, sem passo de build.
