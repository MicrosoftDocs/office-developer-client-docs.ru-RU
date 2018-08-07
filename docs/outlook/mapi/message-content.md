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
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810010"
---
# <a name="message-content"></a><span data-ttu-id="fa129-103">Содержимое сообщения</span><span class="sxs-lookup"><span data-stu-id="fa129-103">Message Content</span></span>

  
  
<span data-ttu-id="fa129-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa129-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa129-105">Существует два возможных кодировки для содержимого сообщения: один с помощью MIME, другой с помощью uuencode.</span><span class="sxs-lookup"><span data-stu-id="fa129-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="fa129-106">MIME — это кодировки.</span><span class="sxs-lookup"><span data-stu-id="fa129-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="fa129-107">В дополнение к этому MAPI определяет свойство каждого получателя, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), который управляет ли данные TNEF должно быть включено в исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa129-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="fa129-108">Так что являются всего четыре способа кодирования содержимого сообщения:</span><span class="sxs-lookup"><span data-stu-id="fa129-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="fa129-109">MIME с TNEF</span><span class="sxs-lookup"><span data-stu-id="fa129-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="fa129-110">MIME-без TNEF</span><span class="sxs-lookup"><span data-stu-id="fa129-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="fa129-111">UUENCODE с TNEF</span><span class="sxs-lookup"><span data-stu-id="fa129-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="fa129-112">UUENCODE без TNEF</span><span class="sxs-lookup"><span data-stu-id="fa129-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="fa129-113">Выбор MIME и uuencode исходящих сообщений не указан.</span><span class="sxs-lookup"><span data-stu-id="fa129-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="fa129-114">Следующие свойства, исключаются из формата TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="fa129-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="fa129-115">Все остальные свойства передаваемого сообщения включаются в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="fa129-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="fa129-116">Следующие рекомендации предназначены для предоставления списка параметров, которые реализации можно решить, как обеспечить поддержку:</span><span class="sxs-lookup"><span data-stu-id="fa129-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="fa129-117">Следует ли кодирование, используя MIME и uuencode для исходящих сообщений: boolean.</span><span class="sxs-lookup"><span data-stu-id="fa129-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="fa129-118">Кодировка исходящих сообщений: string (копируется непосредственно в параметр charset) или перечисление (внутреннее преобразование строку знаков).</span><span class="sxs-lookup"><span data-stu-id="fa129-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

