# Best practice dattiloscritto nel 2025

Impara i più recenti modelli e pratiche dattiloscritti per scrivere codice più pulito.

## Sommario
- [Introduzione] (#Introduzione)
- [1.Usa la modalità rigorosa] (numero 1-utilizzo-timore)
- [2.Usa l'inferenza del tipo] (inferenza di tipo 2-usate)
- [3.Preferisci le interfacce sui tipi] (#3-preter-interfacce-over-types)
- [4.Mantieni i tipi piccoli] (#4-keep-types-Small)
- [5.Utilizzare correttamente i tipi Nullable] (#5-Uso-Nulllable-Types-Properly)
- [6.Leva Generics] (#6-Leverage-Generics)
- [7.Evita `Any` type] (#7-EVID-ANY-TYPE)
- [conclusione] (#conclusione)

## Introduzione

TypeScript continua a evolversi, portando strumenti e pratiche migliori per scrivere applicazioni robuste.In questa guida, esploreremo alcune delle migliori pratiche che ti aiuteranno a scrivere un codice più pulito e più gestibile in TypeScript.

## 1. Usa la modalità rigorosa

La modalità rigorosa di TypeScript consente diverse opzioni di compilatore che rendono il linguaggio più sicuro e più prevedibile.Abilitare la modalità rigorosa ti costringe a essere esplicito con i tipi, prevenendo potenziali errori nel codice.

Per abilitare la modalità rigorosa, aggiungi quanto segue al tuo `tsconfig.json`:

`` `json
{
"CompileRoptions": {
"rigoroso": vero
}
}