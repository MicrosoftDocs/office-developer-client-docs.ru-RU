---
title: Поддержка форматированного текста в исХодящих сообщениях обязанности клиента
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327407"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="f9725-103">Поддержка форматированного текста в исХодящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="f9725-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="f9725-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9725-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9725-105">Клиентские приложения задают свойство **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)), свойство **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или свойство **пр_хтмл** ([PidTagHtml](pidtaghtml-canonical-property.md)) для исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="f9725-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="f9725-106">Клиенты, поддерживающие только обычный текст, задают только свойство **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="f9725-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="f9725-107">Клиенты, поддерживающие формат RTF, могут задавать как свойства **пр_боди** , так и **пр_ртф_компрессед** , или только **пр_ртф_компрессед**, в зависимости от используемого поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f9725-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="f9725-108">Клиенты, поддерживающие HTML, задают свойство **пр_хтмл** .</span><span class="sxs-lookup"><span data-stu-id="f9725-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="f9725-109">Необходимо, чтобы клиент проверит свойство **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) своего хранилища сообщений, чтобы определить, поддерживает ли хранилище RTF.</span><span class="sxs-lookup"><span data-stu-id="f9725-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="f9725-110">Если хранилище сообщений не включено в формат RTF, то клиент, поддерживающий RTF, задает свойства **пр_боди** и **пр_ртф_компрессед** для каждого исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f9725-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="f9725-111">Если хранилище сообщений включено в формат RTF, необходимо задать только свойство **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="f9725-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="f9725-112">**Чтобы настроить ПР_РТФ_КОМПРЕССЕД и убедиться в том, что процесс синхронизации выполняется по мере необходимости, поддерживающих RTF клиентов**</span><span class="sxs-lookup"><span data-stu-id="f9725-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="f9725-113">ВыЗовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **пр_ртф_компрессед** , установив флаги мапи_креате и мапи_модифи.</span><span class="sxs-lookup"><span data-stu-id="f9725-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="f9725-114">МАПИ_КРЕАТЕ гарантирует, что любые новые данные заменяют все старые данные, и МАПИ_МОДИФИ позволяет выполнить эти замены.</span><span class="sxs-lookup"><span data-stu-id="f9725-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="f9725-115">ВыЗовите функцию [врапкомпресседртфстреам](wrapcompressedrtfstream.md) , передав сторе_ункомпрессед_ртф, если хранилище сообщений устанавливает бит сторе_ункомпрессед_ртф в свойстве **пр_сторе_суппорт_маск** , чтобы получить несжатую версию \*\*PR_RTF_COMPRESSED \*\*поток, возвращенный из **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="f9725-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="f9725-116">Запись текстовых данных сообщения в несжатый поток, возвращенный из **врапкомпресседртфстреам**.</span><span class="sxs-lookup"><span data-stu-id="f9725-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="f9725-117">ЗаФиксируйте и освободите несжатые и сжатые потоки.</span><span class="sxs-lookup"><span data-stu-id="f9725-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="f9725-118">На этом шаге, если поставщик хранилища сообщений поддерживает RTF, вы выполнили все необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="f9725-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="f9725-119">При необходимости можно зависеть от поставщика хранилища сообщений для обработки процесса синхронизации и создания свойства **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="f9725-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="f9725-120">Однако если поставщик хранилища сообщений не поддерживает формат RTF, необходимо вызвать функцию [ртфсинк](rtfsync.md) для синхронизации текста с форматированием, УСТАНОВИВ флаг ртф_синк_ртф_чанжед.</span><span class="sxs-lookup"><span data-stu-id="f9725-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

