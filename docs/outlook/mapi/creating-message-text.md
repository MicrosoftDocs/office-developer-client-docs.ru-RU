---
title: Создание текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428006"
---
# <a name="creating-message-text"></a><span data-ttu-id="05488-103">Создание текста сообщения</span><span class="sxs-lookup"><span data-stu-id="05488-103">Creating message text</span></span>

<span data-ttu-id="05488-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05488-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05488-105">Хотя некоторые сообщения состоит только из списка получателей и строки темы, содержимое большинства сообщений, в частности IPM. Сообщения заметок, включая текст.</span><span class="sxs-lookup"><span data-stu-id="05488-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="05488-106">Текст сообщения может быть простым или отформатированный и хранится в трех свойствах: **PR \_ BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="05488-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="05488-107">Если клиент основан на обычном тексте, установите **PR \_ BODY.**</span><span class="sxs-lookup"><span data-stu-id="05488-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="05488-108">Если вы поддерживаете форматированный текст в формате RTF, установите  PR_RTF_COMPRESSED только PR_RTF_COMPRESSED и **PR \_ BODY** в зависимости от используемого поставщика rtF. </span><span class="sxs-lookup"><span data-stu-id="05488-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="05488-109">Когда клиент с RTF использует хранилище сообщений с RTF, он PR_RTF_COMPRESSED **только.**</span><span class="sxs-lookup"><span data-stu-id="05488-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="05488-110">Когда клиент с RTF использует хранилище сообщений, не относя оно к RTF, он задает оба свойства.</span><span class="sxs-lookup"><span data-stu-id="05488-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="05488-111">Если ваш клиент поддерживает HTML, за **установите** PR_HTML свойства.</span><span class="sxs-lookup"><span data-stu-id="05488-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="05488-112">Определение того, поддерживает ли хранилище сообщений формат RICH Text</span><span class="sxs-lookup"><span data-stu-id="05488-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="05488-113">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений, чтобы получить свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="05488-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="05488-114">Проверьте, нет ли STORE_RTF_OK бита.</span><span class="sxs-lookup"><span data-stu-id="05488-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="05488-115">Если STORE_RTF_OK, поставщик rtF поддерживает текст RTF.</span><span class="sxs-lookup"><span data-stu-id="05488-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="05488-116">Если он не установлен, поставщик store сообщений поддерживает только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="05488-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="05488-117">Определение того, поддерживает ли хранилище сообщений HTML</span><span class="sxs-lookup"><span data-stu-id="05488-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="05488-118">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) PR_STORE_SUPPORT_MASK **сообщения.**</span><span class="sxs-lookup"><span data-stu-id="05488-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="05488-119">Проверьте, нет ли STORE_HTML_OK бита.</span><span class="sxs-lookup"><span data-stu-id="05488-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="05488-120">Если STORE_HTML_OK установлен, поставщик службы хранения сообщений поддерживает HTML-текст.</span><span class="sxs-lookup"><span data-stu-id="05488-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-pr_rtf_compressed"></a><span data-ttu-id="05488-121">Настройка \_ pr-RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="05488-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="05488-122">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) сообщения, чтобы открыть свойство **PR_RTF_COMPRESSED,** указав IID_IStream в качестве идентификатора интерфейса и установив флаг MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="05488-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="05488-123">Вызовите функцию [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF в свойстве PR_STORE_SUPPORT_MASK хранения **сообщений.**</span><span class="sxs-lookup"><span data-stu-id="05488-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="05488-124">Выпустите исходный поток, вызывая его метод \*\* IUnknown::Release \*\*.</span><span class="sxs-lookup"><span data-stu-id="05488-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="05488-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="05488-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="05488-126">Вызовите **методы Commit** и **Release** в потоке, возвращаемом **методом OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="05488-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="05488-127">На этом этапе, если поставщик rtF поддерживает RTF, вы сделали все необходимое.</span><span class="sxs-lookup"><span data-stu-id="05488-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="05488-128">Вы можете в зависимости от поставщика содержимого и форматирования сообщений обрабатывать синхронизацию содержимого и форматирования сообщений, а также при необходимости создавать **свойство PR \_ BODY.**</span><span class="sxs-lookup"><span data-stu-id="05488-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="05488-129">В сообщениях с RTF хранится вызов [RTFSync](rtfsync.md) для обработки синхронизации.</span><span class="sxs-lookup"><span data-stu-id="05488-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="05488-130">Если для флага SYNC_BODY_CHANGED RTF установлено SYNC_BODY_CHANGED true, поставщик перекомпьютерит \_ **PR_BODY** свойства.</span><span class="sxs-lookup"><span data-stu-id="05488-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="05488-131">Если ваш поставщик RTF не поддерживает RTF, необходимо также добавить содержимое  сообщений, не относя PR_BODY RTF.</span><span class="sxs-lookup"><span data-stu-id="05488-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-pr_html"></a><span data-ttu-id="05488-132">Настройка PR_HTML</span><span class="sxs-lookup"><span data-stu-id="05488-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="05488-133">Вызовите [метод IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть PR_HTML **с** помощью **интерфейса IStream.**</span><span class="sxs-lookup"><span data-stu-id="05488-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="05488-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="05488-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="05488-135">Вызовите **IStream::Commit** и **IUnknown::Release** в потоке, чтобы зафиксировать изменения и освободить память.</span><span class="sxs-lookup"><span data-stu-id="05488-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-pr_body"></a><span data-ttu-id="05488-136">Настройка PR_BODY</span><span class="sxs-lookup"><span data-stu-id="05488-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="05488-137">Вызовите [метод IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть PR_BODY **с** помощью **интерфейса IStream.**</span><span class="sxs-lookup"><span data-stu-id="05488-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="05488-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="05488-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="05488-139">Вызовите [функцию RTFSync,](rtfsync.md) чтобы синхронизировать текст с форматированием.</span><span class="sxs-lookup"><span data-stu-id="05488-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="05488-140">Так как это новое сообщение, установите флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED, чтобы указать, что версия текста сообщения в виде RTF и обычного текста изменились.</span><span class="sxs-lookup"><span data-stu-id="05488-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="05488-141">**RTFSync** задает несколько связанных свойств, необходимых поставщику store сообщений, например **PR_RTF_IN_SYNC** ([PidTagRtfInSync),](pidtagrtfinsync-canonical-property.md)и запишет их в сообщение.</span><span class="sxs-lookup"><span data-stu-id="05488-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="05488-142">Вызовите **IStream::Commit** и **IUnknown::Release** в потоке, чтобы зафиксировать изменения и освободить память.</span><span class="sxs-lookup"><span data-stu-id="05488-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

