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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348582"
---
# <a name="opening-message-text"></a><span data-ttu-id="a1d14-103">Открытие текста сообщения</span><span class="sxs-lookup"><span data-stu-id="a1d14-103">Opening message text</span></span>

<span data-ttu-id="a1d14-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1d14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1d14-105">Текст сообщения хранится в свойстве текста по отношению к **тексту (PR)\_** или сжатом **RTF\_\_(пр.)** .</span><span class="sxs-lookup"><span data-stu-id="a1d14-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="a1d14-106">Дополнительную информацию можно узнать в **статье\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и сжатом **\_RTF\_** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a1d14-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="a1d14-107">Если вы поддерживаете формат RTF, откройте **ртф_компрессед (пр\_**).</span><span class="sxs-lookup"><span data-stu-id="a1d14-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a1d14-108">Если вы не поддерживаете формат RTF, **откройте\_текст PR**.</span><span class="sxs-lookup"><span data-stu-id="a1d14-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="a1d14-109">Так как текст сообщения может быть большим, независимо от того, отформатирован он или нет, используйте **IMAPIProp:: опенпроперти** , чтобы открыть эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a1d14-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="a1d14-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a1d14-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="a1d14-111">Отображение форматированного текста сообщения</span><span class="sxs-lookup"><span data-stu-id="a1d14-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="a1d14-112">Если вы используете хранилище сообщений с поддержкой не в формате RTF, как указано в разделе отсутствие флага СТОРЕ_РТФ_ОК в свойстве **пр_сторе_суппорт_маск** хранилища ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):</span><span class="sxs-lookup"><span data-stu-id="a1d14-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="a1d14-113">ВыЗовите метод **IMAPIProp::** /PROPS сообщения, чтобы получить свойство **пр_ртф_ин_синк** .</span><span class="sxs-lookup"><span data-stu-id="a1d14-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="a1d14-114">Дополнительные сведения см. в статье [IMAPIProp::](imapiprop-getprops.md) -PROPS and **пр_ртф_ин_синк** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a1d14-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="a1d14-115">ВыЗовите Ртфсинк для синхронизации свойства ПР_БОДИ сообщения с помощью свойства \*\*пр_ртф_компрессед\*\* .</span><span class="sxs-lookup"><span data-stu-id="a1d14-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="a1d14-116">Дополнительные сведения см. в статье [ртфсинк](rtfsync.md), **пр_боди**и **пр_ртф_компрессед**.</span><span class="sxs-lookup"><span data-stu-id="a1d14-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="a1d14-117">Если при вызове метода получения **пр_ртф_ин_синк** произошел сбой, необходимо передать флаг ртф_синк_боди_чанжед, так как свойство не существует или имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="a1d14-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="a1d14-118">Если **ртфсинк** ВОЗВРАЩАЕТ значение true, указывающее, что были сделаны изменения, вызовите метод **IMAPIProp:: SaveChanges** сообщения, чтобы окончательно сохранить их.</span><span class="sxs-lookup"><span data-stu-id="a1d14-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="a1d14-119">Дополнительные сведения см. в разделе [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="a1d14-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="a1d14-120">Независимо от того, используется ли хранилище сообщений с поддержкой RTF:</span><span class="sxs-lookup"><span data-stu-id="a1d14-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="a1d14-121">Call **IMAPIProp:: опенпроперти** , чтобы открыть свойство **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="a1d14-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="a1d14-122">Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и **пр_ртф_компрессед**.</span><span class="sxs-lookup"><span data-stu-id="a1d14-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="a1d14-123">Если **пр_ртф_компрессед** недоступен, вызовите **опенпроперти** , чтобы открыть свойство **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="a1d14-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="a1d14-124">ВыЗовите функцию **врапкомпресседртфстреам** , чтобы создать несжатую версию сжатых данных RTF, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="a1d14-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="a1d14-125">Дополнительные сведения см. в разделе [врапкомпресседртфстреам](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="a1d14-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="a1d14-126">Скопируйте отформатированный текст из потока в соответствующее место формы сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1d14-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="a1d14-127">Отображение обычного текста сообщения</span><span class="sxs-lookup"><span data-stu-id="a1d14-127">To display plain message text</span></span>
  
1. <span data-ttu-id="a1d14-128">ВыЗовите метод **IMAPIProp::** /PROPS сообщения, чтобы получить свойство **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="a1d14-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="a1d14-129">Дополнительные сведения см. в статье [IMAPIProp::](imapiprop-getprops.md)/PROPS.</span><span class="sxs-lookup"><span data-stu-id="a1d14-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="a1d14-130">Если \*\*\*\* параметр PROPS ВОЗВРАЩАЕТ значение пт_еррор для типа свойства в структуре значения свойства или мапи_е_нот_енаугх_мемори, вызовите метод **IMAPIProp:: опенпроперти** этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1d14-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="a1d14-131">Передайте **пр_боди** как тег свойства и иид_истреам в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a1d14-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="a1d14-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a1d14-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="a1d14-133">Скопируйте обычный текст из потока в соответствующее место формы сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1d14-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

