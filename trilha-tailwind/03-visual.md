# 03 - Visual

## Agora voce vai controlar a aparencia

Depois de montar a estrutura, o proximo passo e dar identidade visual.
As categorias mais importantes sao:

- tipografia
- cor
- fundo
- borda
- raio
- sombra
- opacidade

## Tipografia essencial

Classes comuns:

- `text-sm`, `text-base`, `text-lg`, `text-2xl`, `text-4xl`
- `font-medium`, `font-semibold`, `font-bold`
- `leading-6`, `leading-7`, `leading-tight`
- `tracking-tight`, `tracking-wide`
- `text-slate-900`, `text-slate-600`, `text-white`

Exemplo:

```html
<div class="space-y-3">
  <span class="text-sm font-semibold uppercase tracking-wide text-blue-600">
    Destaque
  </span>
  <h1 class="text-4xl font-bold tracking-tight text-slate-950">
    Interfaces mais rapidas de construir
  </h1>
  <p class="max-w-2xl text-base leading-7 text-slate-600">
    Utility-first acelera implementacao sem abrir mao de consistencia visual.
  </p>
</div>
```

## Cor e contraste

Use a cor com intencao:

- texto principal: mais forte
- texto secundario: mais suave
- fundo: neutro
- acento: usado em pontos de foco

Padrao saudavel:

- fundo claro ou escuro consistente
- destaque em uma cor principal
- contraste legivel

## Fundo, borda e sombra

```html
<article class="rounded-3xl border border-slate-200 bg-white p-8 shadow-xl">
  <h2 class="text-xl font-semibold text-slate-900">Card premium</h2>
  <p class="mt-2 text-slate-600">Mais refinamento visual com poucas classes.</p>
</article>
```

Classes uteis:

- `bg-white`, `bg-slate-950`
- `border`, `border-slate-200`
- `rounded-lg`, `rounded-xl`, `rounded-2xl`, `rounded-full`
- `shadow`, `shadow-lg`, `shadow-xl`

## Gradiente e destaque

```html
<section class="rounded-[32px] bg-gradient-to-br from-slate-950 via-slate-900 to-blue-900 p-10 text-white shadow-2xl">
  <h2 class="text-3xl font-bold tracking-tight">Hero principal</h2>
  <p class="mt-3 max-w-xl text-slate-200">
    Gradientes ajudam a criar atmosfera quando usados com moderacao.
  </p>
</section>
```

## Regra de design importante

Nao tente "salvar" um layout ruim com cor e sombra.
Primeiro:

- estrutura boa
- espacamento correto
- hierarquia de titulo e texto

Depois:

- cor
- sombra
- borda

## Exercicio

Pegue o card do modulo 01 e crie 3 variacoes:

1. neutra e corporativa
2. vibrante e moderna
3. minimalista e elegante

Restricao:

- voce nao pode mudar a estrutura, so o visual

## Meta do modulo

Ao fim deste arquivo, voce deve conseguir:

- criar hierarquia tipografica
- usar cor com criterio
- dar acabamento visual sem exagero
