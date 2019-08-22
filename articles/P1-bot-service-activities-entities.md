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
# <a name="entities-and-activity-types"></a><span data-ttu-id="e7fba-104">Typy encji i aktywności</span><span class="sxs-lookup"><span data-stu-id="e7fba-104">Entities and activity types</span></span>

<span data-ttu-id="e7fba-105">Jednostki są częścią działania i dostarczają dodatkowych informacji na temat aktywności lub konwersacji.</span><span class="sxs-lookup"><span data-stu-id="e7fba-105">Entities are a part of an activity, and provide additional information about the activity or conversation.</span></span>

[!include[Entity boilerplate](includes/C1-snippet-entity-boilerplate.md)]

## <a name="entities"></a><span data-ttu-id="e7fba-106">Jednostek</span><span class="sxs-lookup"><span data-stu-id="e7fba-106">Entities</span></span>

<span data-ttu-id="e7fba-107">Właściwość *Entities* w wiadomości to tablica obiektów <a href="http://schema.org/" target="_blank">Schema.org</a> , które są w trakcie otwierania, które umożliwiają wymianę typowych metadanych kontekstowych między kanałem i bota.</span><span class="sxs-lookup"><span data-stu-id="e7fba-107">The *entities* property of a message is an array of open-ended <a href="http://schema.org/" target="_blank">schema.org</a> objects which allows the exchange of common contextual metadata between the channel and bot.</span></span>

### <a name="mention-entities"></a><span data-ttu-id="e7fba-108">Wzmianka o jednostkach</span><span class="sxs-lookup"><span data-stu-id="e7fba-108">Mention entities</span></span> 

<span data-ttu-id="e7fba-109">Wiele kanałów umożliwia bota lub użytkownikowi "wzmianki" w kontekście konwersacji.</span><span class="sxs-lookup"><span data-stu-id="e7fba-109">Many channels support the ability for a bot or user to "mention" someone within the context of a conversation.</span></span>
<span data-ttu-id="e7fba-110">Aby wzmianka o użytkowniku w wiadomości, Wypełnij Właściwość jednostki wiadomości za pomocą obiektu *wzmianki* .</span><span class="sxs-lookup"><span data-stu-id="e7fba-110">To mention a user in a message, populate the message's entities property with a *mention* object.</span></span>
<span data-ttu-id="e7fba-111">Obiekt wzmianki zawiera następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="e7fba-111">The mention object contains these properties:</span></span>

| <span data-ttu-id="e7fba-112">Właściwości</span><span class="sxs-lookup"><span data-stu-id="e7fba-112">Property</span></span> | <span data-ttu-id="e7fba-113">Opis</span><span class="sxs-lookup"><span data-stu-id="e7fba-113">Description</span></span> |
|----|----|
| <span data-ttu-id="e7fba-114">Wpisywać</span><span class="sxs-lookup"><span data-stu-id="e7fba-114">Type</span></span> | <span data-ttu-id="e7fba-115">Typ jednostki ("wzmianka")</span><span class="sxs-lookup"><span data-stu-id="e7fba-115">type of the entity ("mention")</span></span> |
| <span data-ttu-id="e7fba-116">Podany</span><span class="sxs-lookup"><span data-stu-id="e7fba-116">Mentioned</span></span> | <span data-ttu-id="e7fba-117">obiekt konta kanału wskazujący, który użytkownik został wymieniony</span><span class="sxs-lookup"><span data-stu-id="e7fba-117">channel account object that indicates which user was mentioned</span></span> | 
| <span data-ttu-id="e7fba-118">SMS</span><span class="sxs-lookup"><span data-stu-id="e7fba-118">Text</span></span> | <span data-ttu-id="e7fba-119">tekst w obrębie właściwości *Activity. Text* , która reprezentuje samą wzmiankę (może być pusta lub zerowa)</span><span class="sxs-lookup"><span data-stu-id="e7fba-119">text within the *activity.text* property that represents the mention itself (may be empty or null)</span></span> |

<span data-ttu-id="e7fba-120">W tym przykładzie kodu pokazano, jak dodać jednostkę wzmianki do kolekcji Entities.</span><span class="sxs-lookup"><span data-stu-id="e7fba-120">This code example shows how to add a mention entity to the entities collection.</span></span>

# <a name="ctabcs"></a>[<span data-ttu-id="e7fba-121">S #</span><span class="sxs-lookup"><span data-stu-id="e7fba-121">C#</span></span>](#tab/cs)
[!code-csharp[set Mention](includes/code/C1-dotnet-create-messages.cs#setMention)]

