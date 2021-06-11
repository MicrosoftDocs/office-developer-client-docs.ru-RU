---
title: Отрисовка вложения в тексте RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439795"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="031c9-103">Отрисовка вложения в тексте RTF</span><span class="sxs-lookup"><span data-stu-id="031c9-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="031c9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="031c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="031c9-105">Клиенты с богатым текстовым форматом (RTF) могут получать сведения о позиции отрисовки из  текста сообщения RTF, ищем следующую последовательность побега в свойстве PR_RTF_COMPRESSED сообщения[(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="031c9-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="031c9-106">**Поиск сведений о отрисовки в форматированный текст**</span><span class="sxs-lookup"><span data-stu-id="031c9-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="031c9-107">Позвоните **в IMessage::GetAttachmentTable,** чтобы получить доступ к таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="031c9-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="031c9-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="031c9-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="031c9-109">Создайте ограничение свойства, ограничивающее таблицу строками, **PR_RENDERING_POSITION** не равными -1.</span><span class="sxs-lookup"><span data-stu-id="031c9-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="031c9-110">Дополнительные сведения см. **в PR_RENDERING_POSITION** [(PidTagRenderingPosition).](pidtagrenderingposition-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="031c9-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="031c9-111">Call **IMAPITable:::Restrict** to enforce the restriction.</span><span class="sxs-lookup"><span data-stu-id="031c9-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="031c9-112">Дополнительные сведения см. [в iMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="031c9-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="031c9-113">Вызов **IMAPITable::SortTable для** сортировки вложений.</span><span class="sxs-lookup"><span data-stu-id="031c9-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="031c9-114">Дополнительные сведения см. [в iMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="031c9-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="031c9-115">Вызов **IMAPITable::QueryRows,** чтобы получить соответствующие строки.</span><span class="sxs-lookup"><span data-stu-id="031c9-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="031c9-116">Дополнительные сведения см. [в iMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="031c9-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="031c9-117">Вызовите метод **IMAPIProp::OpenProperty** для  получения PR_RTF_COMPRESSED **интерфейса IStream.**</span><span class="sxs-lookup"><span data-stu-id="031c9-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="031c9-118">Дополнительные сведения см. [в iMAPIProp::OpenProperty](imapiprop-openproperty.md) **и PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="031c9-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="031c9-119">Сканируйте поток, ищите местообладатель отрисовки. `\objattph`</span><span class="sxs-lookup"><span data-stu-id="031c9-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="031c9-120">Символ, следующий за этим местом, — это место для следующего вложения в сортировке таблицы.</span><span class="sxs-lookup"><span data-stu-id="031c9-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

