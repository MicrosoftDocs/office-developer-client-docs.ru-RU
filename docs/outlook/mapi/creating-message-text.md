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
# <a name="creating-message-text"></a><span data-ttu-id="cc36d-103">Создание текста сообщения</span><span class="sxs-lookup"><span data-stu-id="cc36d-103">Creating message text</span></span>

<span data-ttu-id="cc36d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc36d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc36d-105">Несмотря на то, что некоторые сообщения состоят только из списка получателей и строки темы, содержимое большинства сообщений, в частности, IPM. Обратите внимание, что в сообщениях есть текст.</span><span class="sxs-lookup"><span data-stu-id="cc36d-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="cc36d-106">Текст сообщения может быть простым или форматированным и храниться в трех свойствах: **\_Body** ([PidTagBody](pidtagbody-canonical-property.md)) **,\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc36d-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="cc36d-107">Если ваш клиент является обычным текстовым, задайте **текст\_** для поля Цена.</span><span class="sxs-lookup"><span data-stu-id="cc36d-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="cc36d-108">Если вы поддерживаете форматирование текста в формате RTF, задайте либо **PR_RTF_COMPRESSED** только, либо **PR_RTF_COMPRESSED** и **\_текст**, в зависимости от используемого поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc36d-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="cc36d-109">Когда клиент, поддерживающий RTF, использует хранилище сообщений с поддержкой RTF, он задается только **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="cc36d-110">Когда клиент с поддержкой RTF использует хранилище сообщений, не поддерживающий RTF, он задает оба свойства.</span><span class="sxs-lookup"><span data-stu-id="cc36d-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="cc36d-111">Если ваш клиент поддерживает HTML, задайте свойство **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="cc36d-112">Определение того, поддерживает ли хранилище сообщений форматированный текст</span><span class="sxs-lookup"><span data-stu-id="cc36d-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="cc36d-113">Вызовите метод [IMAPIProp::-PROPS](imapiprop-getprops.md) хранилища сообщений для получения свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cc36d-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="cc36d-114">Проверьте STORE_RTF_OK бит.</span><span class="sxs-lookup"><span data-stu-id="cc36d-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="cc36d-115">Если установлен STORE_RTF_OK, то поставщик хранилища сообщений поддерживает текст RTF.</span><span class="sxs-lookup"><span data-stu-id="cc36d-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="cc36d-116">Если оно не задано, то поставщик хранилища сообщений поддерживает только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="cc36d-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="cc36d-117">Определение того, поддерживает ли ваше хранилище сообщений HTML</span><span class="sxs-lookup"><span data-stu-id="cc36d-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="cc36d-118">Вызовите метод [IMAPIProp::/PROPS](imapiprop-getprops.md) хранилища сообщений для получения свойства **PR_STORE_SUPPORT_MASK** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="cc36d-119">Проверьте STORE_HTML_OK бит.</span><span class="sxs-lookup"><span data-stu-id="cc36d-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="cc36d-120">Если установлен STORE_HTML_OK, то поставщик хранилища сообщений поддерживает HTML-текст.</span><span class="sxs-lookup"><span data-stu-id="cc36d-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-pr_rtf_compressed"></a><span data-ttu-id="cc36d-121">Настройка RTF_COMPRESSED\_PR</span><span class="sxs-lookup"><span data-stu-id="cc36d-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="cc36d-122">Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_RTF_COMPRESSED** , указав IID_IStream в качестве идентификатора интерфейса и установив флаг MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="cc36d-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="cc36d-123">Вызовите функцию [врапкомпресседртфстреам](wrapcompressedrtfstream.md) , передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF бит задан в свойстве **PR_STORE_SUPPORT_MASK** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc36d-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="cc36d-124">Освободите исходный поток, вызвав его метод \* \* IUnknown:: Release \* \*.</span><span class="sxs-lookup"><span data-stu-id="cc36d-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="cc36d-125">Call — \* \* IStream:: Write \* \* или **IStream:: CopyTo** для записи текста сообщения в поток, возвращенный из **врапкомпресседртфстреам**.</span><span class="sxs-lookup"><span data-stu-id="cc36d-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="cc36d-126">Вызовите методы **commit** и **Release** в потоке, возвращенном из метода **опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="cc36d-127">На этом шаге, если поставщик хранилища сообщений поддерживает RTF, вы выполнили все необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="cc36d-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="cc36d-128">Вы можете зависеть от поставщика хранилища сообщений, чтобы обрабатывать синхронизацию содержимого и форматирования сообщения и при необходимости создавать **свойство\_текста PR** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="cc36d-129">Хранилища сообщений с поддержкой RTF [ртфсинк](rtfsync.md) вызовов для обработки синхронизации.</span><span class="sxs-lookup"><span data-stu-id="cc36d-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="cc36d-130">Если флаг SYNC_BODY_CHANGED\_RTF имеет значение true, то поставщик повторно вычисляет свойство **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="cc36d-131">Если поставщик хранилища сообщений не поддерживает формат RTF, необходимо также добавить содержимое сообщений, не включенных в формат RTF, с помощью свойства **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-pr_html"></a><span data-ttu-id="cc36d-132">Настройка PR_HTML</span><span class="sxs-lookup"><span data-stu-id="cc36d-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="cc36d-133">Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_HTML** с интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="cc36d-134">Call **IStream:: Write** для записи текстовых данных сообщения в поток, возвращенный из **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="cc36d-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="cc36d-135">Вызов **IStream:: Commit** and **IUnknown:: Release** в потоке для фиксации изменений и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="cc36d-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-pr_body"></a><span data-ttu-id="cc36d-136">Настройка PR_BODY</span><span class="sxs-lookup"><span data-stu-id="cc36d-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="cc36d-137">Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_BODY** с интерфейсом **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cc36d-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="cc36d-138">Call **IStream:: Write** для записи текстовых данных сообщения в поток, возвращенный из **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="cc36d-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="cc36d-139">Вызовите функцию [ртфсинк](rtfsync.md) для синхронизации текста с форматированием.</span><span class="sxs-lookup"><span data-stu-id="cc36d-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="cc36d-140">Так как это новое сообщение, установите флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED, чтобы указать, что текст сообщения был изменен как в формате RTF, так и в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="cc36d-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="cc36d-141">**Ртфсинк** задаст несколько связанных свойств, необходимых поставщику хранилища сообщений, например **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), и запишите их в сообщение.</span><span class="sxs-lookup"><span data-stu-id="cc36d-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="cc36d-142">Вызов **IStream:: Commit** and **IUnknown:: Release** в потоке для фиксации изменений и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="cc36d-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

