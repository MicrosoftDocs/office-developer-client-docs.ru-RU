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
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812623"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="a717e-103">Написание несжатого форматированного текста</span><span class="sxs-lookup"><span data-stu-id="a717e-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="a717e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a717e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a717e-105">При подготовке к отправить сообщение с форматированный текст, либо свойства сообщения **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в сжатых или несжатых текст.</span><span class="sxs-lookup"><span data-stu-id="a717e-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="a717e-106">Написание сжатый текст в свойстве **PR_RTF_COMPRESSED** является очень ЦП и может существенно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="a717e-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="a717e-107">Для повышения эффективности отправки сообщения в формате, либо:</span><span class="sxs-lookup"><span data-stu-id="a717e-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="a717e-108">Обновите Процессор, решения, не всегда означает ли.</span><span class="sxs-lookup"><span data-stu-id="a717e-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="a717e-109">Или -</span><span class="sxs-lookup"><span data-stu-id="a717e-109">Or -</span></span>
    
- <span data-ttu-id="a717e-110">Написание несжатую текст в свойстве **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="a717e-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="a717e-111">Процедура настройки **PR_RTF_COMPRESSED** с текстом несжатую — это то же, как для задания с сжатого текста, за исключением.</span><span class="sxs-lookup"><span data-stu-id="a717e-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="a717e-112">При вызове [WrapCompressedRTFStream](wrapcompressedrtfstream.md), задайте в параметре _ulFlags_ флаг STORE_UNCOMPRESSED_RTF.</span><span class="sxs-lookup"><span data-stu-id="a717e-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a717e-113">Установка несжатую текст имеет недостаток, в том, что увеличение размера сообщения.</span><span class="sxs-lookup"><span data-stu-id="a717e-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

