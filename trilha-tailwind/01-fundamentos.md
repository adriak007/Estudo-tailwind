# 01 - Fundamentos

## O que e Tailwind

Tailwind e um framework CSS utility-first. Em vez de escrever muito CSS separado,
voce monta a interface combinando classes pequenas direto no HTML ou no componente.

Exemplo mental:

- `p-4` = padding
- `mt-6` = margin top
- `text-lg` = texto maior
- `bg-slate-900` = fundo escuro
- `rounded-xl` = borda arredondada

## A ideia principal

Voce nao pensa em "vou criar uma classe chamada card".  
Voce pensa em "quais propriedades esse card precisa?".

Em Tailwind, um card simples pode nascer assim:

```html
<div class="max-w-sm rounded-2xl bg-white p-6 shadow-lg">
  <h2 class="text-xl font-semibold text-slate-900">Titulo</h2>
  <p class="mt-2 text-sm text-slate-600">
    Texto secundario do card.
  </p>
  <button class="mt-4 rounded-lg bg-slate-900 px-4 py-2 text-white">
    Continuar
  </button>
</div>
```

## Como ler uma classe

A maioria das classes segue uma logica simples:

- propriedade + valor
- modificador + propriedade + valor

Exemplos:

- `text-center`
- `font-bold`
- `w-full`
- `max-w-xl`
- `md:grid-cols-3`
- `hover:bg-blue-600`

## O mapa mental que voce precisa

Quando olhar para um bloco de classes, tente separar assim:

1. Estrutura: `block`, `flex`, `grid`, `hidden`
2. Tamanho: `w-*`, `h-*`, `max-w-*`
3. Espacamento: `m-*`, `p-*`, `gap-*`
4. Visual: `bg-*`, `text-*`, `border-*`, `shadow-*`
5. Comportamento: `hover:*`, `focus:*`, `md:*`

## Primeira composicao util

```html
<section class="min-h-screen bg-slate-100 px-6 py-12">
  <div class="mx-auto max-w-5xl">
    <div class="rounded-3xl bg-white p-8 shadow-xl">
      <span class="text-sm font-medium text-blue-600">Novo modulo</span>
      <h1 class="mt-3 text-3xl font-bold tracking-tight text-slate-900">
        Aprendendo Tailwind do jeito certo
      </h1>
      <p class="mt-4 max-w-2xl text-base leading-7 text-slate-600">
        Monte interfaces combinando utilitarios pequenos e objetivos.
      </p>
    </div>
  </div>
</section>
```

## O que evitar no comeco

- Decorar centenas de classes sem entender layout
- Pular direto para customizacao
- Usar `@apply` para tudo
- Misturar Tailwind com CSS solto sem criterio

## Exercicio

Monte um card de perfil com:

- avatar circular
- nome
- cargo
- texto curto
- botao principal

Restricoes:

- use apenas utilitarios
- sem CSS separado
- o card precisa ter sombra, espaco interno e cantos arredondados

## Meta do modulo

Quando terminar este arquivo, voce precisa conseguir:

- explicar o que e utility-first
- ler classes sem se perder
- montar um card simples do zero
