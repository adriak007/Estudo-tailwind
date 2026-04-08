# 06 - Componentes

## O problema que aparece no nivel intermediario

No inicio, Tailwind parece simples.
Depois surgem blocos assim:

```html
<button class="inline-flex items-center justify-center rounded-xl bg-blue-600 px-4 py-2 text-sm font-semibold text-white shadow transition hover:bg-blue-700 focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50">
  Botao
</button>
```

Isso ainda esta certo. O problema aparece quando:

- essa string se repete em muitos lugares
- voce precisa de variantes
- cada tela comeca a adaptar do seu proprio jeito

## Como componentizar sem perder a vantagem do Tailwind

Estrutura recomendada:

1. mantenha utilitarios no componente
2. extraia quando a repeticao for real
3. separe base, variante e estado

## Exemplo em React

```tsx
type ButtonProps = {
  children: React.ReactNode
  variant?: "primary" | "secondary"
}

export function Button({ children, variant = "primary" }: ButtonProps) {
  const base =
    "inline-flex items-center justify-center rounded-xl px-4 py-2 text-sm font-semibold transition focus:outline-none focus-visible:ring-2 focus-visible:ring-offset-2"

  const styles = {
    primary: "bg-blue-600 text-white hover:bg-blue-700 focus-visible:ring-blue-500",
    secondary: "bg-slate-200 text-slate-900 hover:bg-slate-300 focus-visible:ring-slate-400",
  }

  return <button className={`${base} ${styles[variant]}`}>{children}</button>
}
```

## Ferramentas comuns para ajudar

Nao sao obrigatorias, mas ajudam bastante:

- `clsx`
- `tailwind-merge`
- `class-variance-authority`

Papel de cada uma:

- `clsx`: montar classes condicionalmente
- `tailwind-merge`: resolver conflitos como `px-4` e `px-6`
- `class-variance-authority`: organizar variantes

## Ordem de leitura das classes

Uma ordem util para manter legibilidade:

1. layout
2. tamanho
3. espacamento
4. tipografia
5. visual
6. estados

Exemplo:

```html
<button class="inline-flex w-full items-center justify-center rounded-xl px-4 py-3 text-sm font-semibold text-white bg-slate-900 shadow-lg transition hover:bg-slate-800">
  Entrar
</button>
```

## Regra importante

Nao extraia componente cedo demais.
Se apareceu uma vez, ainda e so uma implementacao.
Se apareceu tres ou quatro vezes com a mesma estrutura, comece a extrair.

## Exercicio

Crie os seguintes componentes:

1. `Button` com variantes `primary`, `secondary` e `danger`
2. `Badge` com tamanhos `sm` e `md`
3. `Card` com header, body e footer

Desafio extra:

- adicione estados de `loading` e `disabled` no botao

## Meta do modulo

Ao terminar, voce deve conseguir:

- identificar repeticao real
- transformar utilitarios em componente reutilizavel
- manter as classes organizadas em codigo de app
