# 10 - Erros Comuns e Debug

## O que costuma quebrar em Tailwind

Quando algo "nao funciona", normalmente o problema e um destes:

- a classe nao foi gerada
- ha conflito de classes
- o layout foi mal pensado
- o breakpoint esta invertido
- o estado esta aplicado no elemento errado

## Erro 1: classe dinamica demais

Problema:

```tsx
const color = "blue"
return <div className={`bg-${color}-600`} />
```

Risco:

- scanner nao enxerga bem
- manutencao piora

Melhor:

```tsx
const colorMap = {
  blue: "bg-blue-600",
  green: "bg-green-600",
  red: "bg-red-600",
}

return <div className={colorMap.blue} />
```

## Erro 2: usar `flex` onde o problema pedia `grid`

Sintoma:

- cards desalinhados
- quebras estranhas
- alturas inconsistentes

Correcao:

- se ha varias colunas previsiveis, teste `grid`

## Erro 3: espacamento ruim

Sintoma:

- tela parece apertada
- elementos "grudados"
- interface parece amadora

Correcao:

- revise `p-*`
- revise `gap-*`
- adicione `max-w-*`
- teste `leading-*` no texto

## Erro 4: breakpoint na ordem errada

Sintoma:

- mobile quebra
- desktop fica certo, mas celular fica ruim

Correcao:

- comece pelo mobile
- depois aplique `md:*`, `lg:*`, `xl:*`

## Erro 5: `group` e `peer` no lugar errado

Sintoma:

- `group-hover:*` nao dispara
- `peer-invalid:*` nao aparece

Checklist:

- o pai tem `group`?
- o input tem `peer`?
- a classe variante esta no elemento certo?

## Erro 6: classes demais sem ordem

Sintoma:

- voce mesmo nao entende mais o componente

Correcao:

Organize nesta sequencia:

1. display e layout
2. tamanho
3. espacamento
4. tipografia
5. visual
6. estados

## Erro 7: usar recurso avancado cedo demais

Sintoma:

- tudo vira seletor arbitrario
- tudo vira valor arbitrario

Correcao:

- primeiro tente com a escala padrao
- depois use recurso avancado so em casos pontuais

## Rotina curta de debug

1. inspecione o elemento no navegador
2. veja se a classe esta presente
3. veja se outra classe esta vencendo
4. reduza o bloco ate o problema aparecer claramente
5. refaca a composicao em ordem logica

## Perguntas de diagnostico

- o problema e estrutura ou visual?
- o problema aparece em qual breakpoint?
- o estado esta no elemento certo?
- isso realmente precisa de CSS separado?
- o componente ficou repetido e deveria ser extraido?

## Exercicio

Pegue um componente seu e revise procurando:

- classe repetida
- espacamento mal resolvido
- valor arbitrario desnecessario
- variant mal posicionada

Depois reescreva o componente mais limpo.
