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
ms.openlocfilehash: 0f8484e195b1cda8e1d633133cdff89c571d8ecd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811292"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="8a60c-103">Каноническое свойство PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="8a60c-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="8a60c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a60c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a60c-105">Указывает, агрессивности входящую почту направляются в папку нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="8a60c-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a60c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a60c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a60c-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="8a60c-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="8a60c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8a60c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a60c-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="8a60c-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="8a60c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a60c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a60c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8a60c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8a60c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8a60c-112">Area:</span></span>  <br/> |<span data-ttu-id="8a60c-113">Нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="8a60c-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a60c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a60c-114">Remarks</span></span>

<span data-ttu-id="8a60c-115">Это свойство соответствует высокий / низкий / отсутствует filter параметр.</span><span class="sxs-lookup"><span data-stu-id="8a60c-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="8a60c-116">Значение «0xFFFFFFFF» указывает, что фильтрации нежелательной почты не следует применять, но по-прежнему должны применяться черные списки.</span><span class="sxs-lookup"><span data-stu-id="8a60c-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="8a60c-117">Значение «0x80000000» указывает, что все почтовые сообщения, нежелательной почты, за исключением тех сообщения от отправителей в список надежных отправителей или отправленных получателям в список надежных получателей.</span><span class="sxs-lookup"><span data-stu-id="8a60c-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="8a60c-118">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8a60c-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="8a60c-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8a60c-119">**Value**</span></span>|<span data-ttu-id="8a60c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a60c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a60c-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="8a60c-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="8a60c-122">Без фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="8a60c-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="8a60c-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="8a60c-123">0x00000006</span></span>  <br/> |<span data-ttu-id="8a60c-124">Фильтрация низкой нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="8a60c-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="8a60c-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="8a60c-125">0x00000003</span></span>  <br/> |<span data-ttu-id="8a60c-126">Фильтрация высоким нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="8a60c-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="8a60c-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="8a60c-127">0x80000000</span></span>  <br/> |<span data-ttu-id="8a60c-128">Только Надежные списки</span><span class="sxs-lookup"><span data-stu-id="8a60c-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8a60c-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a60c-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a60c-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8a60c-130">Protocol specifications</span></span>

<span data-ttu-id="8a60c-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a60c-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a60c-132">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8a60c-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a60c-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a60c-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a60c-134">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8a60c-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a60c-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8a60c-135">Header files</span></span>

<span data-ttu-id="8a60c-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a60c-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a60c-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a60c-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a60c-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a60c-138">Mapitags.h</span></span>
  
> <span data-ttu-id="8a60c-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8a60c-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a60c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="8a60c-140">See also</span></span>



[<span data-ttu-id="8a60c-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a60c-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a60c-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a60c-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a60c-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a60c-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a60c-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8a60c-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

