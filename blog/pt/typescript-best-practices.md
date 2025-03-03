# Práticas recomendadas de texto datilografado em 2025

Aprenda os mais recentes padrões e práticas do TypeScript para escrever código mais limpo.

## Índice
- [Introdução] (#Introdução)
- [1.Use modo rigoroso] (#1-use-strict-mode)
- [2.Usar inferência de tipo] (INFERÊNCIA DO TIPO DE USUPO#2)
- [3.Prefira interfaces sobre os tipos] (#3-Prefer-Interfaces-Over-types)
- [4.Mantenha os tipos pequenos] (#4-Keep-types-small)
- [5.Use tipos nulláveis ​​corretamente] (#5-use-nullable-types-properly)
- [6.Alavancar genéricos] (#6-Leverage-Generics)
- [7.Evite `qualquer qualquer tipo] (#7-Avoid-anype)
- [Conclusão] (#conclusão)

## Introdução

O TypeScript continua a evoluir, trazendo melhores ferramentas e práticas para escrever aplicativos robustos.Neste guia, exploraremos algumas das melhores práticas que o ajudarão a escrever um código mais limpo e sustentável no TypeScript.

## 1. Use o modo rigoroso

O modo rigoroso do TypeScript permite várias opções de compilador que tornam o idioma mais seguro e previsível.Permitir que o modo rigoroso obriga você a ser explícito com os tipos, impedindo possíveis erros em seu código.

Para ativar o modo rigoroso, adicione o seguinte ao seu `tsconfig.json`:

`` `JSON
{
"Compileroptions": {
"Estrito": verdadeiro
}
}