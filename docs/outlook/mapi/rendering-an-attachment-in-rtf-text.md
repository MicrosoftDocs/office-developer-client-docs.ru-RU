---
title: Отображение вложения в виде текста RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5d8fc10f876408d616c5acefb664ba5d61c927a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562976"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="f3bb3-103">Отображение вложения в виде текста RTF</span><span class="sxs-lookup"><span data-stu-id="f3bb3-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="f3bb3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3bb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3bb3-105">Текст в формате RTF (RTF)-принять во внимание клиентов можно получить сведения положение отображения из текста сообщения RTF ищет следующие escape-последовательность в свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="f3bb3-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="f3bb3-106">**Чтобы найти сведения о визуализации в форматированный текст**</span><span class="sxs-lookup"><span data-stu-id="f3bb3-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="f3bb3-107">Вызов **IMessage::GetAttachmentTable** для доступа к таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="f3bb3-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="f3bb3-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="f3bb3-109">Выполните построение ограничение свойство, которое ограничивает таблицу для строк, имеющих **PR_RENDERING_POSITION** не равно -1.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="f3bb3-110">Для получения дополнительных сведений см **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f3bb3-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="f3bb3-111">Вызов **IMAPITable::Restrict** для установки ограничений.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="f3bb3-112">Для получения дополнительных сведений см [IMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="f3bb3-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="f3bb3-113">Вызов **IMAPITable::SortTable** для сортировки вложения.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="f3bb3-114">Для получения дополнительных сведений см [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="f3bb3-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="f3bb3-115">Вызов **IMAPITable::QueryRows** для получения соответствующих строк.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="f3bb3-116">Для получения дополнительных сведений см [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="f3bb3-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="f3bb3-117">Вызовите метод **IMAPIProp::OpenProperty** сообщений для получения **PR_RTF_COMPRESSED** с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="f3bb3-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="f3bb3-118">Для получения дополнительных сведений см [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="f3bb3-119">Проверка потока, ищите заполнитель визуализации, `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="f3bb3-120">Символ, следующий этот заполнитель — это место для следующего вложения в таблице сортировки.</span><span class="sxs-lookup"><span data-stu-id="f3bb3-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

