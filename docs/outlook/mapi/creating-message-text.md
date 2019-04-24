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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335723"
---
# <a name="creating-message-text"></a><span data-ttu-id="c5b17-103">Создание текста сообщения</span><span class="sxs-lookup"><span data-stu-id="c5b17-103">Creating message text</span></span>

<span data-ttu-id="c5b17-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5b17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5b17-105">Несмотря на то, что некоторые сообщения состоят только из списка получателей и строки темы, содержимое большинства сообщений, в частности, IPM. Обратите внимание, что в сообщениях есть текст.</span><span class="sxs-lookup"><span data-stu-id="c5b17-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="c5b17-106">Текст сообщения может быть простым или форматированным и храниться в трех свойствах: **\_Body** ([PidTagBody](pidtagbody-canonical-property.md)) **,\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c5b17-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="c5b17-107">Если ваш клиент является обычным текстовым, задайте **текст\_** для поля Цена.</span><span class="sxs-lookup"><span data-stu-id="c5b17-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="c5b17-108">Если вы поддерживаете форматирование текста в формате RTF, задайте либо **пр_ртф_компрессед** , либо только текст **пр_ртф_компрессед** и **PR\_**, в зависимости от используемого поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5b17-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="c5b17-109">Когда клиент, поддерживающий RTF, использует хранилище сообщений с поддержкой RTF, он устанавливает только **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="c5b17-110">Когда клиент с поддержкой RTF использует хранилище сообщений, не поддерживающий RTF, он задает оба свойства.</span><span class="sxs-lookup"><span data-stu-id="c5b17-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="c5b17-111">Если ваш клиент поддерживает HTML, задайте свойство **пр_хтмл** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="c5b17-112">Определение того, поддерживает ли хранилище сообщений форматированный текст</span><span class="sxs-lookup"><span data-stu-id="c5b17-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="c5b17-113">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS хранилища сообщений для получения свойства **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c5b17-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="c5b17-114">Проверьте наличие бита СТОРЕ_РТФ_ОК.</span><span class="sxs-lookup"><span data-stu-id="c5b17-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="c5b17-115">Если задано значение СТОРЕ_РТФ_ОК, поставщик хранилища сообщений поддерживает текст RTF.</span><span class="sxs-lookup"><span data-stu-id="c5b17-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="c5b17-116">Если оно не задано, то поставщик хранилища сообщений поддерживает только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="c5b17-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="c5b17-117">Определение того, поддерживает ли ваше хранилище сообщений HTML</span><span class="sxs-lookup"><span data-stu-id="c5b17-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="c5b17-118">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) /PROPS хранилища сообщений, чтобы получить свойство **пр_сторе_суппорт_маск** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="c5b17-119">Проверьте наличие бита СТОРЕ_ХТМЛ_ОК.</span><span class="sxs-lookup"><span data-stu-id="c5b17-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="c5b17-120">Если задано значение СТОРЕ_ХТМЛ_ОК, поставщик хранилища сообщений поддерживает HTML-текст.</span><span class="sxs-lookup"><span data-stu-id="c5b17-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="c5b17-121">Настройка ртф_компрессед\_для PR</span><span class="sxs-lookup"><span data-stu-id="c5b17-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="c5b17-122">ВыЗовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **Пр_ртф_компрессед** , указав иид_истреам в качестве идентификатора интерфейса и установив флаг мапи_креате.</span><span class="sxs-lookup"><span data-stu-id="c5b17-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="c5b17-123">ВыЗовите функцию [врапкомпресседртфстреам](wrapcompressedrtfstream.md) , ПЕРЕДАВ флаг сторе_ункомпрессед_ртф, если установлен бит сторе_ункомпрессед_ртф в свойстве **пр_сторе_суппорт_маск** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c5b17-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="c5b17-124">Освободите исходный поток, вызвав его метод \* \* IUnknown:: Release \* \*.</span><span class="sxs-lookup"><span data-stu-id="c5b17-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="c5b17-125">Call — \* \* IStream:: Write \* \* или **IStream:: CopyTo** для записи текста сообщения в поток, возвращенный из **врапкомпресседртфстреам**.</span><span class="sxs-lookup"><span data-stu-id="c5b17-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="c5b17-126">ВыЗовите методы **commit** и **Release** в потоке, возвращенном из метода **опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="c5b17-127">На этом шаге, если поставщик хранилища сообщений поддерживает RTF, вы выполнили все необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="c5b17-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="c5b17-128">Вы можете зависеть от поставщика хранилища сообщений, чтобы обрабатывать синхронизацию содержимого и форматирования сообщения и при необходимости создавать **свойство\_текста PR** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="c5b17-129">Хранилища сообщений с поддержкой RTF [ртфсинк](rtfsync.md) вызовов для обработки синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c5b17-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="c5b17-130">Если для флага RTF\_синк_боди_чанжед ЗАДАНО значение true, то поставщик повторно вычисляет свойство **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="c5b17-131">Если поставщик хранилища сообщений не поддерживает формат RTF, необходимо также добавить содержимое сообщений, не включенное в формат RTF, с помощью свойства **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="c5b17-132">Set ПР_ХТМЛ</span><span class="sxs-lookup"><span data-stu-id="c5b17-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="c5b17-133">ВыЗовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **пр_хтмл** с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="c5b17-134">Call **IStream:: Write** для записи текстовых данных сообщения в поток, возвращенный из **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="c5b17-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="c5b17-135">Вызов **IStream:: Commit** and **IUnknown:: Release** в потоке для фиксации изменений и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="c5b17-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="c5b17-136">Set ПР_БОДИ</span><span class="sxs-lookup"><span data-stu-id="c5b17-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="c5b17-137">ВыЗовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **пр_боди** с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c5b17-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="c5b17-138">Call **IStream:: Write** для записи текстовых данных сообщения в поток, возвращенный из **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="c5b17-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="c5b17-139">ВыЗовите функцию [ртфсинк](rtfsync.md) для синхронизации текста с форматированием.</span><span class="sxs-lookup"><span data-stu-id="c5b17-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="c5b17-140">Так как это новое сообщение, установите флаги РТФ_СИНК_РТФ_ЧАНЖЕД и РТФ_СИНК_БОДИ_ЧАНЖЕД, чтобы указать, что текст сообщения был изменен как в формате RTF, так и в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="c5b17-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="c5b17-141">**Ртфсинк** задаст несколько связанных свойств, необходимых поставщику хранилища сообщений, например **пр_ртф_ин_синк** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), и запишите их в сообщение.</span><span class="sxs-lookup"><span data-stu-id="c5b17-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="c5b17-142">Вызов **IStream:: Commit** and **IUnknown:: Release** в потоке для фиксации изменений и освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="c5b17-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

