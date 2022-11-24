---
title: ApplyAnimation
description: Primenjuje animaciju na igraču
tags: []
---

## Description

Ova funkcija primenjuje animaciju na igraču.

| Naziv       | Opis                                                                                                                                                                                                                                                                                                   |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| playerid   | ID igrača na kom treba primeniti animaciju                                                                                                                                                                                                                                                            |
| animlib[]  | Biblioteka iz koje se primenjuje animacija                                                                                                                                                                                                                                                    |
| animname[] | Unikatno ime animacije iz biblioteke koja je prethodno određena                                                                                                                                                                                                                                            |
| fDelta     | Brzina animacije (preporučena 4.1)                                                                                                                                                                                                                                                                    |
| loop       | Ako je postavljeno na 1, animacija će se ponoviti. Ako je podešeno na 0, animacija će se reprodukovati jednom.                                                                                                                                                                                                                              |
| lockx      | Ako je postavljeno na 0, igrač se vraća na svoju staru X koordinatu kada se animacija završi (za animacije koje pomeraju igrača kao što je hodanje). 1 ih neće ih vratiti na stari položaj.                                                                                                             |
| locky      | Isto kao gore, ali za Y osu. Trebalo bi da ostane isti kao prethodni parametar.                                                                                                                                                                                                                      |
| freeze     | Podešavanje na 1 će zamrznuti igrača na kraju animacije. 0 neće.                                                                                                                                                                                                                             |
| time       | Tajmer u milisekundama. Za beskrajnu petlju trebalo bi da bude 0.                                                                                                                                                                                                                                               |
| forcesync  | Postavite na 1 da bi server sinhronizovao animaciju sa svim drugim igračima u radijusu za strimovanje (opciono). 2 radi isto kao 1, ali će SAMO primeniti animaciju na strimovane igrače, ali NE i na stvarnog igrača koji se animira (korisno za npc animacije i stalne animacije kada se igrači strimuju) |

## Returns

Ova funkcija uvek vraća pozitivan ishod (true ili 1), čak i ako navedeni igrač ne postoji ili je bilo koji od parametara nevažeći (npr. nevažeća biblioteka).

## Examples

```c
ApplyAnimation(playerid, "PED", "WALK_DRUNK", 4.1, 1, 1, 1, 1, 1, 1);
```

## Notes

:::tip

Opcioni parametar 'forcesync', koji je podrazumevano podešen na 0, u većini slučajeva nije potreban pošto igrači sami sinhronizuju animacije. Parametar 'forcesync' može primorati sve igrače koji mogu da vide 'playerid' da reprodukuju animaciju bez obzira da li igrač izvodi tu animaciju. Ovo je korisno u okolnostima kada igrač ne može sam da sinhronizuje animaciju. Na primer, mogu biti pauzirani.

:::

:::warning

Nevažeća biblioteka animacije će krešovati igru igrača.

:::

## Related Functions

- [ClearAnimations](ClearAnimations): Zaustavlja sve animacije koje određeni igrač obavlja.
- [SetPlayerSpecialAction](SetPlayerSpecialAction): Primenjuje specijalnu akciju nad igračem.
