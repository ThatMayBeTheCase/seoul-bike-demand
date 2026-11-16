# Seoul Bike Demand analysis

## Syfte

Förutsäga hur många hyrcyklar som hyrs ut per timme i Seoul utifrån tid och väder,
och undersöka hur valet av testuppdelning påverkar hur bra modellen verkar vara.

## Datakälla

[Seoul Bike Sharing Demand – UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand)

## Innehåll

1. `1_tid_dag.ipynb` – timme, veckodag och lediga dagar
2. `2_väder.ipynb` – vilka väderfaktorer som spelar roll
3. `3_modeller.ipynb` – jämförelse av modeller (slumpmässig uppdelning)
4. `4_optimering.ipynb` – optimering av Random Forest (kronologisk uppdelning)
5. `5_slutsats.ipynb` – slutsatser

## Kom igång

```bash
pixi install
pixi run jupyter lab
```

## Slutsatser

- Uthyrningen styrs främst av timme, ledig dag och temperatur. Regn sänker den kraftigt.
- Med slumpmässig uppdelning gav Random Forest lägst fel (MAE ca 152).
- När vi testade på årets sista period blev felet ca 261, alltså tydligt sämre.
  Hur modellen testas påverkar resultatet lika mycket som valet av modell.
