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
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808265"
---
# <a name="creating-message-text"></a><span data-ttu-id="a3a4b-103">Создание текста сообщения</span><span class="sxs-lookup"><span data-stu-id="a3a4b-103">Creating message text</span></span>

<span data-ttu-id="a3a4b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3a4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3a4b-105">Несмотря на то, что некоторые сообщения состоят из не более чем список получателей и Тема содержимого большинство сообщений, в частности IPM. Обратите внимание, сообщения, включает в себя текст.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="a3a4b-106">Сообщение может быть обычным или форматированный текст и хранится в три свойства: **связей с Общественностью\_ТЕЛО** ([PidTagBody](pidtagbody-canonical-property.md)), **связей с Общественностью\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3a4b-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="a3a4b-107">Если ваш клиент на основе обычного текста, установите **связей с Общественностью\_ТЕЛО**.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="a3a4b-108">Если вы поддерживаете форматированный текст в форматированный текст (RTF), необходимо задать только **PR_RTF_COMPRESSED** или оба **PR_RTF_COMPRESSED** и **связей с Общественностью\_ТЕЛО**, в зависимости от поставщика хранилища сообщений, которое используется.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="a3a4b-109">Если принять во внимание RTF клиент использует принять во внимание RTF хранилища сообщений, **PR_RTF_COMPRESSED** задает только.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="a3a4b-110">Когда принять во внимание RTF клиент использует хранилище поддерживающими RTF сообщений, задает оба свойства.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="a3a4b-111">Если клиент поддерживает HTML, присвойте свойству **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="a3a4b-112">Определить, поддерживает ли хранения сообщений формат RTF</span><span class="sxs-lookup"><span data-stu-id="a3a4b-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="a3a4b-113">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3a4b-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="a3a4b-114">Проверьте наличие бит STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="a3a4b-115">Если значение STORE_RTF_OK, поставщик хранения сообщений поддерживает текст RTF.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="a3a4b-116">Если не указано, поставщик хранения сообщений поддерживает только обычный текст.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="a3a4b-117">Определить, поддерживает ли хранения сообщений HTML</span><span class="sxs-lookup"><span data-stu-id="a3a4b-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="a3a4b-118">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_STORE_SUPPORT_MASK** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="a3a4b-119">Проверьте наличие бит STORE_HTML_OK.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="a3a4b-120">Если значение STORE_HTML_OK, поставщик хранения сообщений поддерживает HTML-текст.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="a3a4b-121">Установка связей с Общественностью\_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="a3a4b-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="a3a4b-122">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) сообщение, чтобы открыть свойство **PR_RTF_COMPRESSED** , указав IID_IStream идентификатор интерфейса и установка флага MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="a3a4b-123">Вызовите функцию [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF бит задан в свойстве **PR_STORE_SUPPORT_MASK** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="a3a4b-124">Освобождение исходный поток, вызвав его ** функции IUnknown::Release ** метод.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-124">Release the original stream by calling its ** IUnknown::Release ** method.</span></span> 
    
4. <span data-ttu-id="a3a4b-125">Вызвать ** IStream::Write ** или **IStream::CopyTo** для записи текста сообщения в потоке, возвращенный из **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-125">Call either ** IStream::Write ** or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="a3a4b-126">Вызовите методы **Фиксация** и **выпуска** для потока, возвращенный методом **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="a3a4b-127">На этом этапе Если поставщик хранения сообщений поддерживает RTF, выполнен все, что является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="a3a4b-128">Может зависеть от поставщика хранилища сообщений для обработки форматирование и синхронизация содержимого сообщений и для создания **связей с Общественностью\_ТЕЛО** свойства, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="a3a4b-129">Хранилищ принять во внимание RTF сообщений вызов [RTFSync](rtfsync.md) для обработки синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="a3a4b-130">Если RTF\_флаг SYNC_BODY_CHANGED имеет значение TRUE, поставщик будет пересчитывать свойства **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="a3a4b-131">Если поставщик хранилища сообщений не поддерживает формат RTF, необходимо также добавить содержимое сообщения не RTF путем установки свойства **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="a3a4b-132">Набор PR_HTML</span><span class="sxs-lookup"><span data-stu-id="a3a4b-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="a3a4b-133">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть **PR_HTML** свойства с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="a3a4b-134">Вызов **IStream::Write** для записи данных текста сообщения в поток, возвращенный **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="a3a4b-135">Вызовите **IStream::Commit** и **функции IUnknown::Release** потока, чтобы сохранить изменения и освобождать память.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="a3a4b-136">Набор PR_BODY</span><span class="sxs-lookup"><span data-stu-id="a3a4b-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="a3a4b-137">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть **PR_BODY** свойства с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="a3a4b-138">Вызов **IStream::Write** для записи данных текста сообщения в поток, возвращенный **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="a3a4b-139">Вызовите функцию [RTFSync](rtfsync.md) , чтобы синхронизировать текст с форматированием.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="a3a4b-140">Поскольку это новое сообщение, задайте RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED флаги для указания, что изменения RTF и обычного текста версия текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="a3a4b-141">**RTFSync** будет установка нескольких связанных свойств, которые требуется поставщик хранения сообщений, таких как **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) и записи их к сообщению.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="a3a4b-142">Вызовите **IStream::Commit** и **функции IUnknown::Release** потока, чтобы сохранить изменения и освобождать память.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

