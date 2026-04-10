# 04 - Responsivo e Estados

## A logica do Tailwind e mobile-first

Voce escreve primeiro para telas menores.
Depois adiciona ajustes com prefixos como:

- `sm:`
- `md:`
- `lg:`
- `xl:`
- `2xl:`

Exemplo:

```html
<section class="grid grid-cols-1 gap-6 md:grid-cols-2 xl:grid-cols-4">
  <article class="rounded-2xl bg-white p-6 shadow">A</article>
  <article class="rounded-2xl bg-white p-6 shadow">B</article>
  <article class="rounded-2xl bg-white p-6 shadow">C</article>
  <article class="rounded-2xl bg-white p-6 shadow">D</article>
</section>
```

Leitura:

- no mobile: 1 coluna
- em `md`: 2 colunas
- em `xl`: 4 colunas

## Estados interativos

Classes muito usadas:

- `hover:*`
- `focus:*`
- `focus-visible:*`
- `active:*`
- `disabled:*`

Exemplo:

```html
<button class="rounded-xl bg-blue-600 px-5 py-3 font-medium text-white transition hover:bg-blue-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50">
  Salvar
</button>
```

## Group e Peer

Esses dois recursos fazem muita diferenca.

### `group`

Permite estilizar filhos quando o pai entra em estado.

```html
<a href="#" class="group block rounded-2xl bg-white p-6 shadow transition hover:-translate-y-1 hover:shadow-xl">
  <h3 class="text-lg font-semibold text-slate-900 group-hover:text-blue-600">
    Card interativo
  </h3>
  <p class="mt-2 text-slate-600">
    O titulo muda quando o card inteiro recebe hover.
  </p>
</a>
```

### `peer`

Permite estilizar um elemento baseado no estado do irmao marcado como `peer`.

```html
<label class="block">
  <span class="mb-2 block text-sm font-medium text-slate-700">Email</span>
  <input
    type="email"
    class="peer w-full rounded-xl border border-slate-300 px-4 py-3 outline-none focus:border-blue-500"
    placeholder="voce@email.com"
  />
  <span class="mt-2 hidden text-sm text-red-600 peer-invalid:block">
    Digite um email valido.
  </span>
</label>
```

## Dark mode e variantes

Voce tambem pode trabalhar com variantes como:

- `dark:*`
- `group-hover:*`
- `peer-invalid:*`

Essas variantes te ajudam a escrever menos CSS manual.

## Exercicio

Monte um formulario com:

- campo de nome
- campo de email
- botao de envio
- mensagens visuais para hover, focus e erro

Desafio extra:

- em telas maiores, coloque os campos lado a lado

## Meta do modulo

Ao terminar, voce precisa conseguir:

- pensar mobile-first
- aplicar estados sem CSS adicional
- usar `group` e `peer` em situacoes reais
