# 05 - Customizacao

## Quando customizar

Muita gente customiza cedo demais. Isso atrapalha.

Primeiro domine:

- classes padrao
- escala de espacamento
- paleta base
- layout e componentes simples

Depois customiza.

## O que normalmente vale customizar

- cores de marca
- tipografia do projeto
- radius padrao
- sombras principais
- espacamentos recorrentes

## Pense em tokens, nao em telas isoladas

Ruim:

- `azul-da-home`
- `cinza-do-card-x`

Melhor:

- `brand`
- `surface`
- `surface-muted`
- `text-primary`
- `text-secondary`
- `danger`

## Exemplo conceitual de tema

Em projetos diferentes, a sintaxe muda um pouco conforme a versao do Tailwind.
A ideia central, no entanto, continua a mesma: registrar tokens reutilizaveis.

Exemplo no estilo tradicional:

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        brand: "#0f172a",
        accent: "#2563eb",
        surface: "#f8fafc",
      },
      borderRadius: {
        xl2: "1.25rem",
      },
      boxShadow: {
        soft: "0 12px 40px rgba(15, 23, 42, 0.12)",
      },
    },
  },
}
```

Uso:

```html
<section class="rounded-xl2 bg-surface p-8 shadow-soft">
  <h2 class="text-brand">Area customizada</h2>
  <button class="bg-accent text-white">Acao</button>
</section>
```

## `@apply`: use com criterio

`@apply` pode ajudar, mas costuma ser usado em excesso.

Bom uso:

- pequenas abstractions recorrentes
- utilitarios internos de design system

Mau uso:

- recriar CSS tradicional inteiro dentro de classes customizadas
- esconder completamente o que a interface esta fazendo

## Regras praticas de customizacao

- mantenha o nome semantico
- adicione poucas extensoes por vez
- documente tokens recorrentes
- prefira consistencia a liberdade total

## Exercicio

Crie uma identidade simples para um produto ficticio com:

- 1 cor principal
- 1 cor de destaque
- 2 tons de superficie
- 2 niveis de sombra
- 2 radios de borda

Depois reescreva um card usando apenas esses tokens.

## Meta do modulo

Ao fim deste arquivo, voce deve conseguir:

- entender o que vale personalizar
- evitar customizacao sem necessidade
- montar uma base mais consistente para projeto real
