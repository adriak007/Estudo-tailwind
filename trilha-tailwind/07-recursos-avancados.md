# 07 - Recursos Avancados

## Quando voce entra no nivel avancado

O nivel avancado com Tailwind nao e "decorar mais classes".
E saber resolver casos menos triviais sem fugir para CSS manual toda hora.

## Valores arbitrarios

Voce pode usar valores sob medida quando a escala padrao nao cobre bem.

Exemplos:

```html
<div class="w-[420px] max-w-full rounded-[28px] p-[18px]">
  Caixa personalizada
</div>
```

Casos bons:

- um raio muito especifico
- um calculo com `calc(...)`
- um tamanho pontual que faz sentido no layout

Casos ruins:

- inventar numero novo para tudo
- abandonar a escala padrao do projeto

## Seletores arbitrarios

Muito poderoso para estilizar filhos sem sair do fluxo do componente.

```html
<article class="[&_h2]:text-2xl [&_h2]:font-bold [&_p]:mt-3 [&_p]:text-slate-600">
  <h2>Titulo</h2>
  <p>Paragrafo 1</p>
  <p>Paragrafo 2</p>
</article>
```

Outro exemplo util:

```html
<ul class="[&>li]:rounded-xl [&>li]:bg-white [&>li]:p-4 [&>li]:shadow">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

## Data attributes e aria

Muito util em componentes interativos.

```html
<button
  data-state="open"
  class="rounded-xl border px-4 py-2 data-[state=open]:bg-slate-900 data-[state=open]:text-white"
>
  Filtro
</button>
```

```html
<a
  aria-current="page"
  class="text-slate-500 aria-[current=page]:font-bold aria-[current=page]:text-slate-950"
>
  Dashboard
</a>
```

## Before e After

Pseudo-elementos tambem entram no jogo.

```html
<span class="relative pl-4 before:absolute before:left-0 before:top-1/2 before:h-2 before:w-2 before:-translate-y-1/2 before:rounded-full before:bg-emerald-500">
  Online
</span>
```

## Utilitarios proprios

Quando um padrao e recorrente demais, voce pode criar utilitarios internos.

Exemplo conceitual:

```css
@layer utilities {
  .surface-card {
    @apply rounded-2xl bg-white p-6 shadow-xl;
  }
}
```

Isso pode ser util, mas use pouco.
Se tudo vira classe customizada, voce perde a principal vantagem do Tailwind.

## Plugins

Conforme o projeto cresce, alguns plugins podem ajudar em casos especificos.
Exemplos comuns:

- formularios
- tipografia para conteudo rico
- line clamp

Adicione plugin por necessidade real, nao por moda.

## Exercicio

Monte um menu lateral com:

- item ativo por `aria-current`
- grupos expansivos por `data-state`
- marcador visual com `before:`
- cards de conteudo estilizados por seletor arbitrario

## Meta do modulo

Ao fim deste arquivo, voce deve conseguir:

- usar Tailwind alem do basico
- resolver casos pontuais sem exagerar no CSS manual
- reconhecer quando recurso avancado ajuda ou atrapalha
