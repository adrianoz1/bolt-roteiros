# Bolt Videos

Repositório de produção dos vídeos do canal [Bolt](https://www.youtube.com/@boltjz).

Aqui ficam as pautas, pesquisas, versões de roteiro, storyboards, arquivos visuais e projetos de animação usados em cada vídeo. O objetivo é manter o processo criativo organizado sem transformar a escrita em uma linha de montagem.

## Estrutura

```text
brand/                     Identidade visual e referências do canal
docs/                      Guias editoriais e fluxo de produção
skills/                    Skills do Bolt versionadas com o projeto
templates/                 Modelos para iniciar novos vídeos
videos/
  001-nome-do-video/
    README.md               Estado e decisões do vídeo
    pesquisa/               Fontes, notas e transcrições
    roteiro/                Versões graváveis do roteiro
    storyboard/             Planejamento visual por cena
    assets/
      imagens/
      audio/
      video/
    remotion/               Projeto de animação, quando necessário
```

## Fluxo de trabalho

1. Criar uma pasta numerada em `videos/` a partir dos modelos em `templates/`.
2. Definir tese, conflito e promessa antes de escrever o roteiro.
3. Guardar fontes e fatos verificáveis em `pesquisa/`.
4. Versionar o roteiro como `roteiro-v1.md`, `roteiro-v2.md` e assim por diante.
5. Marcar a versão aprovada como `roteiro-final.md`; não sobrescrever a história das versões.
6. Criar o storyboard somente depois de estabilizar a narração.
7. Produzir imagens e animações dentro da pasta do próprio vídeo.
8. Registrar decisões relevantes no `README.md` do vídeo.

## Convenções

- Textos e nomes de produção em português brasileiro.
- Pastas em `kebab-case` e numeradas na ordem de produção.
- Arquivos brutos pesados não entram no Git; consulte `.gitignore`.
- Fontes externas devem ter URL, autoria, data de acesso e a afirmação que sustentam.
- Experiências pessoais do Bolt nunca devem ser inventadas.
- Blocos comerciais só entram no roteiro quando houver campanha e briefing confirmados.

## Skills do projeto

- [`bolt-roteiros`](skills/bolt-roteiros/SKILL.md): escrita e revisão de roteiros na voz do Bolt.
- [`bolt-visuais`](skills/bolt-visuais/SKILL.md): planejamento e geração de memes, recortes e assets transparentes para a edição acelerada do canal.

As cópias em `skills/` são as versões canônicas e ficam registradas no Git. Para uso pelo Codex, elas também podem ser instaladas no diretório global de skills.

## Vídeos

| ID | Projeto | Estado |
| --- | --- | --- |
| 001 | [A IA pode matar novas linguagens de programação?](videos/001-ia-linguagens/README.md) | Roteiro v1 |
