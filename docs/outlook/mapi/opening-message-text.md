---
title: Открытие текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407538"
---
# <a name="opening-message-text"></a><span data-ttu-id="c1603-103">Открытие текста сообщения</span><span class="sxs-lookup"><span data-stu-id="c1603-103">Opening message text</span></span>

<span data-ttu-id="c1603-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1603-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1603-105">Текст сообщения хранится либо в свойстве **PR \_ BODY,** либо **в свойстве PR \_ RTF \_ COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="c1603-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="c1603-106">Дополнительные сведения см. в pr **\_ BODY** [(PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** [(PidTagHtml)](pidtaghtml-canonical-property.md)и **PR \_ RTF \_ COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c1603-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="c1603-107">Если вы поддерживаете формат Rich Text (RTF), откройте **\_ PR-RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="c1603-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="c1603-108">Если вы не поддерживаете RTF, откройте **PR \_ BODY**.</span><span class="sxs-lookup"><span data-stu-id="c1603-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="c1603-109">Поскольку текст сообщения может быть большим независимо от формата или нет, используйте **IMAPIProp::OpenProperty** для открытия этих свойств.</span><span class="sxs-lookup"><span data-stu-id="c1603-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="c1603-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c1603-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="c1603-111">Отображение отформатированный текст сообщения</span><span class="sxs-lookup"><span data-stu-id="c1603-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="c1603-112">Если вы используете хранилище сообщений, не вступив в RTF, о чем свидетельствует  отсутствие флага STORE_RTF_OK в свойстве PR_STORE_SUPPORT_MASK магазина[(PidTagStoreSupportMask):](pidtagstoresupportmask-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c1603-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="c1603-113">Чтобы получить свойство PR_RTF_IN_SYNC, позвоните по методу **IMAPIProp::GetProps.** </span><span class="sxs-lookup"><span data-stu-id="c1603-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="c1603-114">Дополнительные сведения см. [в странице IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** [(PidTagRtfInSync).](pidtagrtfinsync-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c1603-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="c1603-115">Позвоните в RTFSync, чтобы синхронизировать свойство PR_BODY сообщения с **свойством PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="c1603-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="c1603-116">Дополнительные сведения см. в [RTFSync,](rtfsync.md) **PR_BODY** и **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="c1603-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="c1603-117">Передай флаг RTF_SYNC_BODY_CHANGED, если вызов  на PR_RTF_IN_SYNC не удалось, так как свойство не существует или задано false.</span><span class="sxs-lookup"><span data-stu-id="c1603-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="c1603-118">Если **RTFSync** вернул TRUE , указав, что были внесены изменения, позвоните по методу **IMAPIProp::SaveChanges** для их постоянного хранения.</span><span class="sxs-lookup"><span data-stu-id="c1603-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="c1603-119">Дополнительные сведения см. [в iMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="c1603-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="c1603-120">Независимо от того, используете ли вы хранилище сообщений, в курсе RTF:</span><span class="sxs-lookup"><span data-stu-id="c1603-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="c1603-121">Чтобы открыть свойство PR_RTF_COMPRESSED, позвоните в **IMAPIProp::OpenProperty.** </span><span class="sxs-lookup"><span data-stu-id="c1603-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="c1603-122">Дополнительные сведения см. [в iMAPIProp::OpenProperty](imapiprop-openproperty.md) **и PR_RTF_COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="c1603-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="c1603-123">Если **PR_RTF_COMPRESSED** недоступны, позвоните **в OpenProperty,** чтобы открыть **свойство PR_BODY.**</span><span class="sxs-lookup"><span data-stu-id="c1603-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="c1603-124">Вызов **функции WrapCompressedRTFStream** для создания некомпрессивной версии сжатых данных RTF, если это доступно.</span><span class="sxs-lookup"><span data-stu-id="c1603-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="c1603-125">Дополнительные сведения см. в [ссылке WrapCompressedRTFStream.](wrapcompressedrtfstream.md)</span><span class="sxs-lookup"><span data-stu-id="c1603-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="c1603-126">Скопируйте отформатированный текст из потока в соответствующее место в форме сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1603-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="c1603-127">Отображение простого текста сообщения</span><span class="sxs-lookup"><span data-stu-id="c1603-127">To display plain message text</span></span>
  
1. <span data-ttu-id="c1603-128">Чтобы получить свойство PR_BODY, позвоните по методу **IMAPIProp::GetProps.** </span><span class="sxs-lookup"><span data-stu-id="c1603-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="c1603-129">Дополнительные сведения см. [в iMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="c1603-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="c1603-130">Если **GetProps** возвращает PT_ERROR для типа свойства в структуре значения свойства или MAPI_E_NOT_ENOUGH_MEMORY, позвоните в **метод IMAPIProp::OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="c1603-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="c1603-131">**Передай PR_BODY** как тег свойства и IID_IStream как идентификатор интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c1603-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="c1603-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="c1603-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="c1603-133">Скопируйте простой текст из потока в соответствующее место в форме сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1603-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

