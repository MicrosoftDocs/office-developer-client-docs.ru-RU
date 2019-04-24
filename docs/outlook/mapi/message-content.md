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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357003"
---
# <a name="message-content"></a><span data-ttu-id="e7712-103">Содержимое сообщения</span><span class="sxs-lookup"><span data-stu-id="e7712-103">Message Content</span></span>

  
  
<span data-ttu-id="e7712-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7712-105">Существует две возможные кодировки для содержимого сообщения: один использует MIME, другой с помощью кодировки UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="e7712-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="e7712-106">Кодировка MIME предпочтительна.</span><span class="sxs-lookup"><span data-stu-id="e7712-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="e7712-107">Кроме того, MAPI определяет свойство для каждого получателя, **пр_сенд_рич_инфо** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), которое определяет, следует ли включать в исходящие сообщения сведения TNEF.</span><span class="sxs-lookup"><span data-stu-id="e7712-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="e7712-108">Таким образом, существует четыре способа кодирования содержимого сообщений:</span><span class="sxs-lookup"><span data-stu-id="e7712-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="e7712-109">MIME с ФОРМАТом TNEF</span><span class="sxs-lookup"><span data-stu-id="e7712-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="e7712-110">MIME без формата TNEF</span><span class="sxs-lookup"><span data-stu-id="e7712-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="e7712-111">Кодировка uuencode с ФОРМАТом TNEF</span><span class="sxs-lookup"><span data-stu-id="e7712-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="e7712-112">Кодировка uuencode без формата TNEF</span><span class="sxs-lookup"><span data-stu-id="e7712-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="e7712-113">Не указано, как выбрать MIME или uuencode для исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="e7712-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="e7712-114">Следующие свойства исключены из TNEF: **\*пр_сендер_**, **пр_аттач_дата_\***, **пр_боди**.</span><span class="sxs-lookup"><span data-stu-id="e7712-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="e7712-115">Все другие свойства передающего сообщение включены в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="e7712-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="e7712-116">Приведенные ниже рекомендации предназначены для предоставления списка параметров, которые может решить реализация:</span><span class="sxs-lookup"><span data-stu-id="e7712-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="e7712-117">Необходимость кодирования исходящих сообщений с помощью MIME или uuencode: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e7712-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="e7712-118">Набор символов, используемый для исходящих сообщений: строка (копируется непосредственно в параметр CharSet) или перечисление (внутреннее преобразование осуществляется в строку Charset).</span><span class="sxs-lookup"><span data-stu-id="e7712-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

