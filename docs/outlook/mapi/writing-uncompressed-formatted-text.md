---
title: Написание несжатого форматированного текста
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325755"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="03d9b-103">Написание несжатого форматированного текста</span><span class="sxs-lookup"><span data-stu-id="03d9b-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="03d9b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03d9b-105">При подготовке к отправке сообщения с форматированным текстом установите для свойства **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в сжатом или несжатом тексте.</span><span class="sxs-lookup"><span data-stu-id="03d9b-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="03d9b-106">Запись сжатого текста в свойстве **пр_ртф_компрессед** очень трудоемкая операция ЦП и может значительно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="03d9b-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="03d9b-107">Чтобы увеличить производительность при отправке отформатированных сообщений, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="03d9b-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="03d9b-108">Обновление ЦП, решение, которое не всегда плаусибле.</span><span class="sxs-lookup"><span data-stu-id="03d9b-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="03d9b-109">Также</span><span class="sxs-lookup"><span data-stu-id="03d9b-109">Or -</span></span>
    
- <span data-ttu-id="03d9b-110">Запись несжатого текста в свойстве **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="03d9b-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="03d9b-111">Процедура настройки **пр_ртф_компрессед** с несжатым текстом аналогична процедуре для установки сжатого текста с одним исключением.</span><span class="sxs-lookup"><span data-stu-id="03d9b-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="03d9b-112">При вызове [врапкомпресседртфстреам](wrapcompressedrtfstream.md)установите флаг сторе_ункомпрессед_ртф в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="03d9b-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="03d9b-113">Недостаток несжатого текста имеет недостаток в том, что он увеличивает размер сообщений.</span><span class="sxs-lookup"><span data-stu-id="03d9b-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

