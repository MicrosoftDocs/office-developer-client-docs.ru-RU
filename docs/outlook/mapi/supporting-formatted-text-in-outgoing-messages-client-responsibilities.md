---
title: Поддержка форматированный текст в обязанности клиента исходящих сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431605"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="24d52-103">Поддержка форматированный текст в исходящих сообщениях: обязанности клиента</span><span class="sxs-lookup"><span data-stu-id="24d52-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="24d52-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24d52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24d52-105">Клиентские приложения устанавливают свойство **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **свойство PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **свойство PR_HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)для исходяшего сообщения.</span><span class="sxs-lookup"><span data-stu-id="24d52-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="24d52-106">Клиенты, которые поддерживают только обычный текст, устанавливают **только PR_BODY** свойства.</span><span class="sxs-lookup"><span data-stu-id="24d52-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="24d52-107">Клиенты с RTF могут устанавливать свойства  PR_BODY и **PR_RTF_COMPRESSED** или только PR_RTF_COMPRESSED в зависимости от используемого поставщика rtF.</span><span class="sxs-lookup"><span data-stu-id="24d52-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="24d52-108">Клиенты, которые знают HTML, **PR_HTML** свойства.</span><span class="sxs-lookup"><span data-stu-id="24d52-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="24d52-109">Клиенту важно проверить свойство PR_STORE_SUPPORT_MASK[(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)чтобы определить, поддерживает ли хранилище RTF. </span><span class="sxs-lookup"><span data-stu-id="24d52-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="24d52-110">Если хранилище сообщений не имеет RTF-данных, клиент с  RTF задает свойства PR_BODY и **PR_RTF_COMPRESSED** для каждого исходяшего сообщения.</span><span class="sxs-lookup"><span data-stu-id="24d52-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="24d52-111">Если хранилище сообщений имеет RTF-данные, необходимо PR_RTF_COMPRESSED только свойство. </span><span class="sxs-lookup"><span data-stu-id="24d52-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="24d52-112">**Чтобы настроить PR_RTF_COMPRESSED и убедиться, что синхронизация происходит по мере необходимости, клиенты с RTF**</span><span class="sxs-lookup"><span data-stu-id="24d52-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="24d52-113">Вызовите метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть **свойство PR_RTF_COMPRESSED,** установив MAPI_CREATE и MAPI_MODIFY флаги.</span><span class="sxs-lookup"><span data-stu-id="24d52-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="24d52-114">MAPI_CREATE все новые данные заменяют все старые данные, MAPI_MODIFY позволяет их заменять.</span><span class="sxs-lookup"><span data-stu-id="24d52-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="24d52-115">Вызовите функцию [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) передав STORE_UNCOMPRESSED_RTF, если хранилище сообщений задает бит STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK,** чтобы получить несмещенную версию потока PR_RTF_COMPRESSED, возвращаемого **из OpenProperty.** </span><span class="sxs-lookup"><span data-stu-id="24d52-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="24d52-116">Запишите текстовые данные сообщения в несхваченный поток, возвращенный **wrapCompressedRTFStream.**</span><span class="sxs-lookup"><span data-stu-id="24d52-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="24d52-117">Зафиксировать и освободить несжатые и сжатые потоки.</span><span class="sxs-lookup"><span data-stu-id="24d52-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="24d52-118">На этом этапе, если поставщик rtF поддерживает RTF, вы сделали все необходимое.</span><span class="sxs-lookup"><span data-stu-id="24d52-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="24d52-119">Для обработки процесса синхронизации и создания свойства PR_BODY при  необходимости можно использовать поставщика PR_BODY сообщений.</span><span class="sxs-lookup"><span data-stu-id="24d52-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="24d52-120">Однако если поставщик RTF не поддерживает RTF, необходимо вызвать функцию [RTFSync,](rtfsync.md) чтобы синхронизировать текст с форматированием, установив флаг RTF_SYNC_RTF_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="24d52-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

