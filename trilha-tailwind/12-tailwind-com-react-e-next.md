# 12 - Tailwind com React e Next

## Ideia central

Em React e Next, Tailwind funciona melhor quando as classes ficam perto do componente.
Voce pensa em UI como composicao:

- componente
- props
- variantes
- estados

## Regra boa para componente

Mantenha no mesmo lugar:

- markup
- classes
- logica visual

Evite espalhar demais o estilo entre muitos arquivos sem necessidade.

## Exemplo simples de componente

```tsx
type BadgeProps = {
  tone?: "neutral" | "success" | "danger"
  children: React.ReactNode
}

export function Badge({ tone = "neutral", children }: BadgeProps) {
  const tones = {
    neutral: "bg-slate-100 text-slate-800",
    success: "bg-emerald-100 text-emerald-700",
    danger: "bg-red-100 text-red-700",
  }

  return (
    <span className={`inline-flex rounded-full px-3 py-1 text-xs font-semibold ${tones[tone]}`}>
      {children}
    </span>
  )
}
```

## Quando extrair variante

Extraia variante quando:

- a mesma estrutura aparece varias vezes
- a diferenca entre versoes e previsivel
- ha risco de conflito de classes

## `clsx` e `tailwind-merge`

Padrao comum:

```tsx
import clsx from "clsx"
import { twMerge } from "tailwind-merge"

function cn(...inputs: Array<string | false | null | undefined>) {
  return twMerge(clsx(inputs))
}
```

Uso:

```tsx
<button
  className={cn(
    "rounded-xl px-4 py-2 font-medium transition",
    primary && "bg-blue-600 text-white hover:bg-blue-700",
    full && "w-full"
  )}
>
  Salvar
</button>
```

## Estrutura de pastas sugerida

Exemplo simples:

```txt
components/
  ui/
    button.tsx
    badge.tsx
    card.tsx
app/
  dashboard/
  pricing/
lib/
  cn.ts
```

## Boas praticas

- extraia utilitario `cn` se usar classes condicionais
- mantenha variantes previsiveis
- evite componente com vinte props de estilo
- prefira pequenas composicoes
- documente os componentes base

## Erro comum em app real

Componente monstro:

- muitas props
- muitas variantes
- muita logica visual em um arquivo so

Melhor:

- componentes menores
- composicao por partes
- design system simples

## Exercicio

Crie em React ou Next:

1. `Button`
2. `Input`
3. `Card`
4. `SectionTitle`

Depois use esses componentes em uma tela de dashboard.
