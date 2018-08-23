---
title: Каноническое свойство PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7d4337105b2dcae94956f0b1badf66c663467dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565664"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="68a67-103">Каноническое свойство PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="68a67-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="68a67-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68a67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68a67-105">Указывает, агрессивности входящую почту направляются в папку нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="68a67-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68a67-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="68a67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68a67-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="68a67-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="68a67-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="68a67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68a67-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="68a67-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="68a67-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="68a67-110">Data type:</span></span>  <br/> |<span data-ttu-id="68a67-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="68a67-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="68a67-112">Область:</span><span class="sxs-lookup"><span data-stu-id="68a67-112">Area:</span></span>  <br/> |<span data-ttu-id="68a67-113">Нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="68a67-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68a67-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="68a67-114">Remarks</span></span>

<span data-ttu-id="68a67-115">Это свойство соответствует высокий / низкий / отсутствует filter параметр.</span><span class="sxs-lookup"><span data-stu-id="68a67-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="68a67-116">Значение «0xFFFFFFFF» указывает, что фильтрации нежелательной почты не следует применять, но по-прежнему должны применяться черные списки.</span><span class="sxs-lookup"><span data-stu-id="68a67-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="68a67-117">Значение «0x80000000» указывает, что все почтовые сообщения, нежелательной почты, за исключением тех сообщения от отправителей в список надежных отправителей или отправленных получателям в список надежных получателей.</span><span class="sxs-lookup"><span data-stu-id="68a67-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="68a67-118">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="68a67-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="68a67-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68a67-119">**Value**</span></span>|<span data-ttu-id="68a67-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68a67-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68a67-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="68a67-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="68a67-122">Без фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="68a67-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="68a67-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="68a67-123">0x00000006</span></span>  <br/> |<span data-ttu-id="68a67-124">Фильтрация низкой нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="68a67-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="68a67-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="68a67-125">0x00000003</span></span>  <br/> |<span data-ttu-id="68a67-126">Фильтрация высоким нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="68a67-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="68a67-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="68a67-127">0x80000000</span></span>  <br/> |<span data-ttu-id="68a67-128">Только Надежные списки</span><span class="sxs-lookup"><span data-stu-id="68a67-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="68a67-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="68a67-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68a67-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="68a67-130">Protocol specifications</span></span>

<span data-ttu-id="68a67-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68a67-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68a67-132">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="68a67-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68a67-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68a67-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68a67-134">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="68a67-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68a67-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="68a67-135">Header files</span></span>

<span data-ttu-id="68a67-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68a67-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="68a67-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="68a67-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="68a67-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="68a67-138">Mapitags.h</span></span>
  
> <span data-ttu-id="68a67-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="68a67-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68a67-140">См. также</span><span class="sxs-lookup"><span data-stu-id="68a67-140">See also</span></span>



[<span data-ttu-id="68a67-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="68a67-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68a67-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="68a67-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68a67-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="68a67-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68a67-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="68a67-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

