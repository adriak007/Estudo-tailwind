# 08 - Performance e Projeto Final

## Problemas reais em projeto de verdade

Depois que voce aprende Tailwind, os erros mudam.
Nao sao mais erros de sintaxe. Sao erros de manutencao.

## Boas praticas de performance e manutencao

### 1. Nao monte classes dinamicas invisiveis para o scanner

Evite coisas como:

```tsx
const color = "blue"
const classes = `bg-${color}-600`
```

Isso costuma dificultar a geracao correta das classes.
Prefira mapear explicitamente:

```tsx
const styles = {
  blue: "bg-blue-600",
  red: "bg-red-600",
  green: "bg-green-600",
}
```

### 2. Mantenha consistencia de tokens

Se cada tela usa um azul diferente, o projeto vira bagunca.

### 3. Evite repeticao silenciosa

Repetiu demais:

- extraia componente
- documente variante
- defina padrao

### 4. Revise acessibilidade

Checklist minimo:

- contraste legivel
- foco visivel
- estados `disabled` claros
- hierarquia de titulo correta
- hit area confortavel para clique

### 5. Debug visual com criterio

Quando algo quebrar:

1. inspecione o elemento
2. veja qual classe esta vencendo
3. procure conflito de tamanho, display ou gap
4. teste removendo classes aos poucos

## Projeto final sugerido

Escolha um dos tres:

### Projeto 1: Landing page

Objetivo:

- hero
- secao de beneficios
- cards de preco
- FAQ
- footer

Voce pratica:

- layout
- hierarquia visual
- responsividade

### Projeto 2: Dashboard

Objetivo:

- sidebar
- header
- cards de metricas
- tabela simples
- filtros

Voce pratica:

- grid
- estados
- componentes reutilizaveis

### Projeto 3: Tela de autenticacao + area logada

Objetivo:

- login
- validacao visual
- menu lateral
- lista de itens

Voce pratica:

- formularios
- `peer`
- `aria-*`
- composicao de componentes

## Criterios para considerar o projeto bom

- mobile primeiro
- classes legiveis
- espaco consistente
- componentes repetidos extraidos
- sem excesso de CSS separado
- foco visivel nos elementos interativos

## Plano de 14 dias

1. Dia 1: fundamentos
2. Dia 2: repetir fundamentos sem olhar
3. Dia 3: layout
4. Dia 4: montar pagina simples
5. Dia 5: visual
6. Dia 6: replicar uma tela do Dribbble ou Figma
7. Dia 7: responsivo e estados
8. Dia 8: formulario completo
9. Dia 9: customizacao
10. Dia 10: componentes
11. Dia 11: variantes
12. Dia 12: recursos avancados
13. Dia 13: projeto final
14. Dia 14: refatoracao e revisao

## Fechamento

Se voce concluir os exercicios desta trilha com pratica real, ja sai do nivel iniciante.
O salto seguinte vem de repeticao:

- copiar interfaces
- refazer sem olhar
- extrair componentes melhores a cada projeto

Proximo passo natural:

- criar exemplos praticos em HTML
- criar exemplos em React
- criar uma mini biblioteca de componentes
