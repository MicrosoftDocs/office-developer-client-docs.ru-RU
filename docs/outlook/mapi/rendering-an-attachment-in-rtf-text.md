---
title: Отображение вложения в тексте в формате RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280362"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="e1451-103">Отображение вложения в тексте в формате RTF</span><span class="sxs-lookup"><span data-stu-id="e1451-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="e1451-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1451-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1451-105">Клиенты, поддерживающие формат RTF, могут получать сведения о позициях отображения из текста сообщений в формате RTF, найдя следующую escape-последовательность в свойстве **пр_ртф_компрессед** сообщения ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="e1451-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="e1451-106">**Размещение информации для отображения в форматированном тексте**</span><span class="sxs-lookup"><span data-stu-id="e1451-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="e1451-107">Call **iMessage:: жетаттачменттабле** для доступа к таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="e1451-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="e1451-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="e1451-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="e1451-109">Создайте ограничение свойства, которое ограничит таблицу строками, у которых значение параметра **пр_рендеринг_поситион** не равно – 1.</span><span class="sxs-lookup"><span data-stu-id="e1451-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="e1451-110">Дополнительные сведения см. в статье **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1451-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="e1451-111">Вызов **IMAPITable:: Ограничьте** для применения ограничения.</span><span class="sxs-lookup"><span data-stu-id="e1451-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="e1451-112">Для получения дополнительных сведений обратитесь к разделу [IMAPITable:: restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="e1451-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="e1451-113">Call **IMAPITable:: сорттабле** для сортировки вложений.</span><span class="sxs-lookup"><span data-stu-id="e1451-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="e1451-114">Дополнительные сведения см. в разделе [IMAPITable:: сорттабле](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="e1451-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="e1451-115">Call **IMAPITable:: QueryRows** для получения соответствующих строк.</span><span class="sxs-lookup"><span data-stu-id="e1451-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="e1451-116">Дополнительные сведения см. в разделе [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e1451-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="e1451-117">ВыЗовите метод **IMAPIProp:: опенпроперти** , чтобы получить **пр_ртф_компрессед** с интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="e1451-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="e1451-118">Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и **пр_ртф_компрессед**.</span><span class="sxs-lookup"><span data-stu-id="e1451-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="e1451-119">ПроСканируйте поток, выполняя поиск заполнителя отображения `\objattph`,.</span><span class="sxs-lookup"><span data-stu-id="e1451-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="e1451-120">Символ после этого заполнителя — это место для следующего вложения в таблице сортировки.</span><span class="sxs-lookup"><span data-stu-id="e1451-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

