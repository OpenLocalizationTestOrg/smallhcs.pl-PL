---
title: Encje i typy działań | Dokumenty Microsoft
description: Encje i typy działań.
keywords: wzmianka o jednostkach, typach aktywności, zużywaniu jednostek
author: ivorb
ms.author: v-ivorb
manager: kamrani
ms.topic: article
ms.service: bot-service
ms.subservice: sdk
ms.date: 03/01/2018
ms.openlocfilehash: d4f8eb7c66c90dc7df7c09738d931b44057ef593
ms.sourcegitcommit: b7432e53415fba697a23cad2d7e2dc4e0d2b89c9
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/22/2019
ms.locfileid: "6606632"
---
# <a name="entities-and-activity-types"></a>Typy encji i aktywności

Jednostki są częścią działania i dostarczają dodatkowych informacji na temat aktywności lub konwersacji.

[!include[Entity boilerplate](includes/C1-snippet-entity-boilerplate.md)]

## <a name="entities"></a>Jednostek

Właściwość *Entities* w wiadomości to tablica obiektów <a href="http://schema.org/" target="_blank">Schema.org</a> , które są w trakcie otwierania, które umożliwiają wymianę typowych metadanych kontekstowych między kanałem i bota.

### <a name="mention-entities"></a>Wzmianka o jednostkach 

Wiele kanałów umożliwia bota lub użytkownikowi "wzmianki" w kontekście konwersacji.
Aby wzmianka o użytkowniku w wiadomości, Wypełnij Właściwość jednostki wiadomości za pomocą obiektu *wzmianki* .
Obiekt wzmianki zawiera następujące właściwości:

| Właściwości | Opis |
|----|----|
| Wpisywać | Typ jednostki ("wzmianka") |
| Podany | obiekt konta kanału wskazujący, który użytkownik został wymieniony | 
| SMS | tekst w obrębie właściwości *Activity. Text* , która reprezentuje samą wzmiankę (może być pusta lub zerowa) |

W tym przykładzie kodu pokazano, jak dodać jednostkę wzmianki do kolekcji Entities.

# <a name="ctabcs"></a>[S #](#tab/cs)
[!code-csharp[set Mention](includes/code/C1-dotnet-create-messages.cs#setMention)]

