---
title: Содержимое сообщений
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
# <a name="message-content"></a><span data-ttu-id="c86be-103">Содержимое сообщений</span><span class="sxs-lookup"><span data-stu-id="c86be-103">Message Content</span></span>

  
  
<span data-ttu-id="c86be-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c86be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c86be-105">Существует два возможных кодирования контента сообщений: одна — с помощью MIME, другая — с помощью uuencode.</span><span class="sxs-lookup"><span data-stu-id="c86be-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="c86be-106">MIME является предпочтительным кодом.</span><span class="sxs-lookup"><span data-stu-id="c86be-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="c86be-107">Кроме того, MAPI определяет свойство на одного получателя **PR_SEND_RICH_INFO** [(PidTagSendRichInfo),](pidtagsendrichinfo-canonical-property.md)которое определяет, следует ли включать сведения TNEF в исходящую информацию.</span><span class="sxs-lookup"><span data-stu-id="c86be-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="c86be-108">Таким образом, существует в общей сложности четыре способа кодить содержимое сообщений:</span><span class="sxs-lookup"><span data-stu-id="c86be-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="c86be-109">MIME с TNEF</span><span class="sxs-lookup"><span data-stu-id="c86be-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="c86be-110">MIME без TNEF</span><span class="sxs-lookup"><span data-stu-id="c86be-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="c86be-111">uuencode с TNEF</span><span class="sxs-lookup"><span data-stu-id="c86be-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="c86be-112">uuencode без TNEF</span><span class="sxs-lookup"><span data-stu-id="c86be-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="c86be-113">Как выбрать MIME или uuencode для исходящие сообщения, не указывается.</span><span class="sxs-lookup"><span data-stu-id="c86be-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="c86be-114">Из TNEF исключаются следующие свойства: **PR_SENDER_, \*** **PR_ATTACH_DATA_, \*** **PR_BODY.**</span><span class="sxs-lookup"><span data-stu-id="c86be-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="c86be-115">Все другие свойства передаваемых сообщений включены в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="c86be-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="c86be-116">Следующие предложения предназначены для предоставления списка параметров, которые реализация может решить, как поддерживать:</span><span class="sxs-lookup"><span data-stu-id="c86be-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="c86be-117">Следует ли кодировать с помощью MIME или uuencode для исходящие сообщения: boolean.</span><span class="sxs-lookup"><span data-stu-id="c86be-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="c86be-118">Набор символов для исходящие сообщения: строка (скопированная непосредственно на параметр charset) или переустановка (переведенная внутренне на строку charset).</span><span class="sxs-lookup"><span data-stu-id="c86be-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

