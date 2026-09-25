# Especificação de assets

## Formato padrão

- PNG com canal alfa real.
- Espaço de cor sRGB.
- Alta resolução suficiente para zoom de edição.
- Assunto centralizado na própria área útil, com margem transparente entre 5% e 10%.
- Silhueta completa e bordas utilizáveis sobre fundo claro ou escuro.

## Tamanhos sugeridos

- Cabeça ou reação: `1600 × 1600 px`.
- Meio-corpo: `1600 × 2000 px`.
- Corpo inteiro: `1600 × 2400 px`.
- Objeto ou prop: `1600 × 1600 px`.
- Elemento horizontal: até `2400 × 1400 px`.

Use esses tamanhos como referência, não como obrigação. Preserve proporção e resolução quando a fonte fornecida for menor.

## Transparência

Um arquivo atende ao padrão somente quando:

- possui canal alfa;
- há pixels realmente transparentes fora do assunto;
- não existe branco, preto, cinza ou padrão quadriculado fingindo transparência;
- não há halo colorido do fundo original;
- cabelos, fumaça e bordas semitransparentes permanecem legíveis.

## Recorte deliberadamente simples

O estilo aceita recortes secos e memes de baixa resolução, mas não aceita fundo residual acidental. “Tosco” descreve a energia da montagem; não é desculpa para um arquivo inutilizável.

## Texto e interfaces

- Texto animado deve ser criado na edição ou no Remotion.
- Screenshots reais devem permanecer editáveis ou ser guardados também em sua versão original.
- Se um asset precisar de óculos, chapéu, cigarro fictício ou outro prop animável, gere o prop separado quando houver possibilidade de movimento independente.

## Nomes

Use nomes descritivos em `kebab-case`:

```text
reacao-programador-desconfiado-pb.png
gato-confuso-corpo-inteiro.png
mascote-pixel-oculos.png
oculos-pixel-preto.png
```

Evite `imagem-1.png`, `final-final.png` e nomes baseados apenas na ferramenta usada.

## Verificação antes da entrega

1. Abrir sobre fundo claro e escuro.
2. Confirmar que a transparência é real.
3. Reduzir para aproximadamente 25% e verificar leitura.
4. Conferir se nenhuma parte relevante foi cortada.
5. Garantir que texto e fundo não foram incorporados por engano.
6. Registrar a origem quando o asset vier de material externo.

