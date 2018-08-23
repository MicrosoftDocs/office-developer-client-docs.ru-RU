---
title: Содержимое сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586083"
---
# <a name="message-content"></a><span data-ttu-id="6cb6d-103">Содержимое сообщения</span><span class="sxs-lookup"><span data-stu-id="6cb6d-103">Message Content</span></span>

  
  
<span data-ttu-id="6cb6d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cb6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cb6d-105">Существует два возможных кодировки для содержимого сообщения: один с помощью MIME, другой с помощью uuencode.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="6cb6d-106">MIME — это кодировки.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="6cb6d-107">В дополнение к этому MAPI определяет свойство каждого получателя, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), который управляет ли данные TNEF должно быть включено в исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="6cb6d-108">Так что являются всего четыре способа кодирования содержимого сообщения:</span><span class="sxs-lookup"><span data-stu-id="6cb6d-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="6cb6d-109">MIME с TNEF</span><span class="sxs-lookup"><span data-stu-id="6cb6d-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="6cb6d-110">MIME-без TNEF</span><span class="sxs-lookup"><span data-stu-id="6cb6d-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="6cb6d-111">UUENCODE с TNEF</span><span class="sxs-lookup"><span data-stu-id="6cb6d-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="6cb6d-112">UUENCODE без TNEF</span><span class="sxs-lookup"><span data-stu-id="6cb6d-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="6cb6d-113">Выбор MIME и uuencode исходящих сообщений не указан.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="6cb6d-114">Следующие свойства, исключаются из формата TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="6cb6d-115">Все остальные свойства передаваемого сообщения включаются в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="6cb6d-116">Следующие рекомендации предназначены для предоставления списка параметров, которые реализации можно решить, как обеспечить поддержку:</span><span class="sxs-lookup"><span data-stu-id="6cb6d-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="6cb6d-117">Следует ли кодирование, используя MIME и uuencode для исходящих сообщений: boolean.</span><span class="sxs-lookup"><span data-stu-id="6cb6d-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="6cb6d-118">Кодировка исходящих сообщений: string (копируется непосредственно в параметр charset) или перечисление (внутреннее преобразование строку знаков).</span><span class="sxs-lookup"><span data-stu-id="6cb6d-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

