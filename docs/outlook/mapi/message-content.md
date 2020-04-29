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
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435462"
---
# <a name="message-content"></a><span data-ttu-id="658ad-103">Содержимое сообщения</span><span class="sxs-lookup"><span data-stu-id="658ad-103">Message Content</span></span>

  
  
<span data-ttu-id="658ad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="658ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="658ad-105">Существует две возможные кодировки для содержимого сообщения: один использует MIME, другой с помощью кодировки UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="658ad-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="658ad-106">Кодировка MIME предпочтительна.</span><span class="sxs-lookup"><span data-stu-id="658ad-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="658ad-107">Кроме того, MAPI определяет свойство для каждого получателя, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), которое определяет, следует ли включать в исходящие сообщения сведения TNEF.</span><span class="sxs-lookup"><span data-stu-id="658ad-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="658ad-108">Таким образом, существует четыре способа кодирования содержимого сообщений:</span><span class="sxs-lookup"><span data-stu-id="658ad-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="658ad-109">MIME с форматом TNEF</span><span class="sxs-lookup"><span data-stu-id="658ad-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="658ad-110">MIME без формата TNEF</span><span class="sxs-lookup"><span data-stu-id="658ad-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="658ad-111">Кодировка uuencode с форматом TNEF</span><span class="sxs-lookup"><span data-stu-id="658ad-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="658ad-112">Кодировка uuencode без формата TNEF</span><span class="sxs-lookup"><span data-stu-id="658ad-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="658ad-113">Не указано, как выбрать MIME или uuencode для исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="658ad-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="658ad-114">Следующие свойства исключены из TNEF: **\*PR_SENDER_**, **PR_ATTACH_DATA_\*** **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="658ad-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="658ad-115">Все другие свойства передающего сообщение включены в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="658ad-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="658ad-116">Приведенные ниже рекомендации предназначены для предоставления списка параметров, которые может решить реализация:</span><span class="sxs-lookup"><span data-stu-id="658ad-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="658ad-117">Необходимость кодирования исходящих сообщений с помощью MIME или uuencode: Boolean.</span><span class="sxs-lookup"><span data-stu-id="658ad-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="658ad-118">Набор символов, используемый для исходящих сообщений: строка (копируется непосредственно в параметр CharSet) или перечисление (внутреннее преобразование осуществляется в строку Charset).</span><span class="sxs-lookup"><span data-stu-id="658ad-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

