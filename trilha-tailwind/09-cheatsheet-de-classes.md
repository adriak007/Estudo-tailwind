# 09 - Cheatsheet de Classes

## Como usar esta cola

Este arquivo nao substitui pratica.
Use assim:

1. tente montar sem olhar
2. travou, consulte a categoria
3. feche a cola e refaca

## Estrutura e display

- `block`
- `inline-block`
- `hidden`
- `flex`
- `inline-flex`
- `grid`
- `inline-grid`

## Alinhamento com flex

- `items-start`
- `items-center`
- `items-end`
- `justify-start`
- `justify-between`
- `justify-center`
- `flex-col`
- `flex-wrap`

Padrao util:

```html
<div class="flex items-center justify-between gap-4"></div>
```

## Grid

- `grid-cols-1`
- `grid-cols-2`
- `grid-cols-3`
- `md:grid-cols-2`
- `xl:grid-cols-4`
- `col-span-2`

Padrao util:

```html
<section class="grid gap-6 md:grid-cols-2 xl:grid-cols-3"></section>
```

## Espacamento

- `p-2`, `p-4`, `p-6`, `p-8`
- `px-4`, `py-2`
- `m-2`, `mt-4`, `mb-6`
- `gap-2`, `gap-4`, `gap-6`, `gap-8`
- `space-y-4`

## Tamanho

- `w-full`
- `h-full`
- `min-h-screen`
- `max-w-sm`
- `max-w-xl`
- `max-w-6xl`
- `size-10`

## Posicionamento

- `relative`
- `absolute`
- `sticky`
- `top-0`
- `inset-0`
- `z-10`
- `z-50`

## Tipografia

- `text-sm`
- `text-base`
- `text-lg`
- `text-2xl`
- `text-4xl`
- `font-medium`
- `font-semibold`
- `font-bold`
- `leading-6`
- `leading-7`
- `tracking-tight`

## Cor e fundo

- `text-slate-900`
- `text-slate-600`
- `text-white`
- `bg-white`
- `bg-slate-100`
- `bg-slate-900`
- `bg-blue-600`

## Borda e sombra

- `border`
- `border-slate-200`
- `rounded-lg`
- `rounded-xl`
- `rounded-2xl`
- `rounded-full`
- `shadow`
- `shadow-lg`
- `shadow-xl`

## Responsividade

- `sm:*`
- `md:*`
- `lg:*`
- `xl:*`
- `2xl:*`

Exemplo:

```html
<div class="px-4 py-6 md:px-8 lg:px-10"></div>
```

## Estados

- `hover:*`
- `focus:*`
- `focus-visible:*`
- `active:*`
- `disabled:*`
- `group-hover:*`
- `peer-invalid:*`
- `dark:*`

## Classes compostas que voce vai repetir muito

### Card

```html
<article class="rounded-2xl border border-slate-200 bg-white p-6 shadow-lg"></article>
```

### Botao principal

```html
<button class="rounded-xl bg-blue-600 px-4 py-2 font-medium text-white transition hover:bg-blue-700"></button>
```

### Container

```html
<div class="mx-auto w-full max-w-6xl px-6"></div>
```

### Input

```html
<input class="w-full rounded-xl border border-slate-300 px-4 py-3 outline-none focus:border-blue-500" />
```

## Regra de memorizacao

Se voce quer decorar menos, memorize familias:

- layout
- espacamento
- tipografia
- cor
- interacao

Nao memorize aleatoriamente.
