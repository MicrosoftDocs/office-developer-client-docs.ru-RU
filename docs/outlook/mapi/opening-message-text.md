---
title: Открытие текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810066"
---
# <a name="opening-message-text"></a><span data-ttu-id="413cd-103">Открытие текста сообщения</span><span class="sxs-lookup"><span data-stu-id="413cd-103">Opening message text</span></span>

<span data-ttu-id="413cd-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="413cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="413cd-105">Текст сообщения, хранится в его **связей с Общественностью\_ТЕЛО** свойство или **связей с Общественностью\_RTF\_СЖАТЫЙ** свойство.</span><span class="sxs-lookup"><span data-stu-id="413cd-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="413cd-106">Дополнительные сведения можно **связей с Общественностью\_ТЕЛО** ([PidTagBody](pidtagbody-canonical-property.md)), **связей с Общественностью\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **связей с Общественностью\_RTF\_СЖАТЫЙ** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="413cd-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="413cd-107">Если вы поддерживаете форматированный текст (RTF), откройте **связей с Общественностью\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="413cd-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="413cd-108">Если вы не поддерживает формат RTF, откройте **связей с Общественностью\_ТЕЛО**.</span><span class="sxs-lookup"><span data-stu-id="413cd-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="413cd-109">Так как текстовое сообщение могут занимать много места, независимо от того, является ли он имеет формат, используйте **IMAPIProp::OpenProperty** для открытия этих свойств.</span><span class="sxs-lookup"><span data-stu-id="413cd-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="413cd-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="413cd-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="413cd-111">Чтобы отобразить форматированный текст сообщения</span><span class="sxs-lookup"><span data-stu-id="413cd-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="413cd-112">При использовании хранилища принять во внимание сообщений не RTF, как указано в отсутствие флага STORE_RTF_OK в свойстве магазина **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="413cd-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="413cd-113">Вызов метода **IMAPIProp::GetProps** сообщения для получения свойства **PR_RTF_IN_SYNC** .</span><span class="sxs-lookup"><span data-stu-id="413cd-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="413cd-114">Для получения дополнительных сведений см [IMAPIProp::GetProps](imapiprop-getprops.md) и **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="413cd-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="413cd-115">Вызов RTFSync для синхронизации свойство PR_BODY сообщения со свойством **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="413cd-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="413cd-116">Для получения дополнительных сведений см [RTFSync](rtfsync.md), **PR_BODY**и **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="413cd-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="413cd-117">PASS RTF_SYNC_BODY_CHANGED флаг, если не удалось выполнить вызов для получения **PR_RTF_IN_SYNC** , так как свойство не существует, либо он имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="413cd-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="413cd-118">Если **RTFSync** возвращает значение TRUE, указывающего на то, что изменения — вызов метода **IMAPIProp::SaveChanges** сообщение без возможности восстановления их хранения.</span><span class="sxs-lookup"><span data-stu-id="413cd-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="413cd-119">Для получения дополнительных сведений см [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="413cd-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="413cd-120">Независимо от того, является ли вы используете принять во внимание RTF сообщение хранения:</span><span class="sxs-lookup"><span data-stu-id="413cd-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="413cd-121">Вызовите **IMAPIProp::OpenProperty** , чтобы открыть свойство **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="413cd-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="413cd-122">Для получения дополнительных сведений см [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="413cd-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="413cd-123">Если **PR_RTF_COMPRESSED** не поддерживается, вызовите **OpenProperty** для открытия свойство **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="413cd-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="413cd-124">Вызовите функцию **WrapCompressedRTFStream** для создания несжатую версию сжатых данных RTF, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="413cd-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="413cd-125">Для получения дополнительных сведений см [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="413cd-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="413cd-126">Скопируйте форматированного текста в потоке в соответствующее место в форме сообщения.</span><span class="sxs-lookup"><span data-stu-id="413cd-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="413cd-127">Для отображения текста обычные сообщения</span><span class="sxs-lookup"><span data-stu-id="413cd-127">To display plain message text</span></span>
  
1. <span data-ttu-id="413cd-128">Вызов метода **IMAPIProp::GetProps** сообщения для получения свойства **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="413cd-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="413cd-129">Для получения дополнительных сведений см [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="413cd-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="413cd-130">Если в структуре значение свойства или MAPI_E_NOT_ENOUGH_MEMORY **GetProps** возвращает либо PT_ERROR для типа свойства, вызовите метод **IMAPIProp::OpenProperty** сообщение.</span><span class="sxs-lookup"><span data-stu-id="413cd-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="413cd-131">Передайте **PR_BODY** как свойство tag и IID_IStream идентификатор интерфейса.</span><span class="sxs-lookup"><span data-stu-id="413cd-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="413cd-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="413cd-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="413cd-133">Скопируйте текст из потока в соответствующее место в форме сообщения.</span><span class="sxs-lookup"><span data-stu-id="413cd-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

