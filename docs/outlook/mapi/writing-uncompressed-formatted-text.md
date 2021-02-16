---
title: Написание несформатированный форматированный текст
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426326"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="e00e8-103">Написание несформатированный форматированный текст</span><span class="sxs-lookup"><span data-stu-id="e00e8-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="e00e8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e00e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e00e8-105">При подготовке к отправке сообщения с форматированный текст установите для свойства **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)сжатие или несжатие текста.</span><span class="sxs-lookup"><span data-stu-id="e00e8-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="e00e8-106">Запись сжатого текста в **PR_RTF_COMPRESSED** является очень интенсивной операцией ЦП и может существенно повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="e00e8-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="e00e8-107">Чтобы повысить производительность отправки отформатированные сообщения, сформатированные либо:</span><span class="sxs-lookup"><span data-stu-id="e00e8-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="e00e8-108">Обновите ЦП— решение, которое не всегда можно обуявить.</span><span class="sxs-lookup"><span data-stu-id="e00e8-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="e00e8-109">Или -</span><span class="sxs-lookup"><span data-stu-id="e00e8-109">Or -</span></span>
    
- <span data-ttu-id="e00e8-110">Запишите несмеченный текст в **PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="e00e8-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="e00e8-111">Процедура настройки **PR_RTF_COMPRESSED** с несжатием текста та же, что и для установки сжатого текста за одним исключением.</span><span class="sxs-lookup"><span data-stu-id="e00e8-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="e00e8-112">При [вызове WrapCompressedRTFStream](wrapcompressedrtfstream.md)установите флаг STORE_UNCOMPRESSED_RTF в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e00e8-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e00e8-113">Недостаток установки несмеченного текста заключается в том, что он увеличивает размер сообщений.</span><span class="sxs-lookup"><span data-stu-id="e00e8-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

