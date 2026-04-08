# 02 - Layout

## O bloco mais importante do aprendizado

Se voce domina layout, metade do Tailwind fica facil.
As classes mais importantes desta fase sao:

- `flex`
- `grid`
- `gap-*`
- `p-*`
- `m-*`
- `w-*`
- `h-*`
- `min-h-*`
- `max-w-*`
- `mx-auto`

## Quando usar flex

Use `flex` quando os itens estao em uma linha ou coluna e a relacao entre eles e mais linear.

Exemplo:

```html
<div class="flex items-center justify-between gap-4 rounded-xl bg-white p-4 shadow">
  <div>
    <h2 class="font-semibold text-slate-900">Plano Pro</h2>
    <p class="text-sm text-slate-500">Acesso completo</p>
  </div>
  <button class="rounded-lg bg-slate-900 px-4 py-2 text-white">
    Assinar
  </button>
</div>
```

## Quando usar grid

Use `grid` quando voce tem linhas e colunas ou quando quer distribuir blocos de forma mais previsivel.

```html
<section class="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
  <article class="rounded-2xl bg-white p-6 shadow">Card 1</article>
  <article class="rounded-2xl bg-white p-6 shadow">Card 2</article>
  <article class="rounded-2xl bg-white p-6 shadow">Card 3</article>
</section>
```

## Espacamento: regra pratica

Tailwind funciona muito bem quando o espacamento segue escala.

Voce vai usar o tempo todo:

- `p-4`, `p-6`, `p-8`
- `px-4`, `py-2`
- `mt-2`, `mt-4`, `mt-6`
- `gap-3`, `gap-4`, `gap-6`, `gap-8`

Se a tela esta "apertada", normalmente o problema esta aqui:

- padding insuficiente
- gap ruim
- largura maxima faltando

## Largura e centragem

Padrao muito comum:

```html
<div class="mx-auto w-full max-w-6xl px-6">
  Conteudo centralizado
</div>
```

Leitura:

- `w-full`: ocupa toda a largura disponivel
- `max-w-6xl`: limita a largura
- `mx-auto`: centraliza horizontalmente
- `px-6`: cria respiro lateral

## Layout de pagina completo

```html
<div class="min-h-screen bg-slate-100">
  <header class="border-b border-slate-200 bg-white">
    <div class="mx-auto flex max-w-6xl items-center justify-between px-6 py-4">
      <strong class="text-slate-900">Minha App</strong>
      <nav class="flex gap-4 text-sm text-slate-600">
        <a href="#">Inicio</a>
        <a href="#">Produtos</a>
        <a href="#">Contato</a>
      </nav>
    </div>
  </header>

  <main class="mx-auto grid max-w-6xl gap-6 px-6 py-8 lg:grid-cols-[240px_1fr]">
    <aside class="rounded-2xl bg-white p-6 shadow">Sidebar</aside>
    <section class="rounded-2xl bg-white p-6 shadow">Conteudo principal</section>
  </main>
</div>
```

## Decisao rapida: flex ou grid

Use `flex` se:

- a organizacao e em linha ou coluna
- voce quer alinhar e distribuir poucos elementos
- a direcao muda facilmente

Use `grid` se:

- ha varios cards
- ha colunas previsiveis
- o layout parece uma matriz

## Exercicio

Monte uma pagina com:

- header
- sidebar
- area principal
- tres cards em grid
- footer

Desafio extra:

- mobile em coluna
- desktop com sidebar fixa ao lado

## Meta do modulo

Quando terminar, voce deve conseguir olhar um layout e decidir:

- quais blocos sao `flex`
- quais blocos sao `grid`
- onde entra `gap`
- onde precisa de `max-w-*`
