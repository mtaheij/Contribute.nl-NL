---
title: Markdown-koppen
description: Beschrijft de vereisten voor Markdown-koppen.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084452"
---
# <a name="markdown-headings"></a>Markdown-koppen

De volgende validatievereisten zijn van toepassing op koppen in OPS Markdown-bestanden.

## <a name="h1"></a>H1

`H1` verwijst naar de eerste kop in een Markdown-bestand. Bij publicatie naar docs.microsoft.com wordt H1 boven aan de pagina weergegeven in een groot lettertype.

U maakt een H1 door een regel te beginnen met één hash (`#`), gevolgd door een spatie en de tekst van de kop. Dit is bijvoorbeeld de H1 van dit artikel:

```md
# Markdown headings
```

De volgende regels zijn van toepassing op H1-koppen:

- Het bestand moet een H1 bevatten.
- Er kan slechts één H1 zijn.
- De H1 mag niet leeg zijn.

  ```markdown
  # 
  This is not allowed.
  ```
- Tussen de `#` en de inhoud van de H1 moet een spatie staan. Een H1 zonder spatie wordt niet als een kop weergegeven op de gepubliceerde pagina.

  ```markdown
  #This looks bad on the site.
  ```
- De H1 moet de eerste inhoud in het bestand zijn na de YML-kop met metagegevens. Inhoud, zoals tekst of afbeeldingen, tussen het einde van de YML-kop en de H1 is niet toegestaan.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- Het HTML-element voor koppen op het eerste niveau, `<h1>`, mag niet worden gebruikt. Gebruik de Markdown-syntaxis (`# `).
- De H1 mag niet langer dan 100 tekens zijn. Dit is een stijlrichtlijn.

## <a name="h2---h6"></a>H2 - H6

H2 (`## `) tot en met H6 (`###### `) zijn toegestaan in OPS. Gebruik de Markdown-koppen, niet de HTML (`<h2>` - `<h6>`), om koppen te maken.
