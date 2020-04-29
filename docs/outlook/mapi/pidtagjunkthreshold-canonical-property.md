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
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326854"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="b7d06-103">Каноническое свойство PidTagJunkThreshold</span><span class="sxs-lookup"><span data-stu-id="b7d06-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="b7d06-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7d06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7d06-105">Указывает, как активно входящую почту следует отправлять в папку нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="b7d06-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7d06-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b7d06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7d06-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="b7d06-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="b7d06-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b7d06-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7d06-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="b7d06-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="b7d06-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b7d06-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7d06-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b7d06-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b7d06-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b7d06-112">Area:</span></span>  <br/> |<span data-ttu-id="b7d06-113">Нежелательная почта</span><span class="sxs-lookup"><span data-stu-id="b7d06-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7d06-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7d06-114">Remarks</span></span>

<span data-ttu-id="b7d06-115">Это свойство соответствует параметру фильтра "высокий/мин/нет/нет".</span><span class="sxs-lookup"><span data-stu-id="b7d06-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="b7d06-116">Значение "0xFFFFFFFF" указывает на то, что не следует применять фильтрацию нежелательной почты, однако заблокированные списки по-прежнему должны быть применены.</span><span class="sxs-lookup"><span data-stu-id="b7d06-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="b7d06-117">Значение "0x80000000" указывает на то, что все сообщения являются спамом, за исключением сообщений от отправителей в списке надежных отправителей или отправленных получателям в списке надежных получателей.</span><span class="sxs-lookup"><span data-stu-id="b7d06-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="b7d06-118">Для этого используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b7d06-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="b7d06-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b7d06-119">**Value**</span></span>|<span data-ttu-id="b7d06-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7d06-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7d06-121">Равен</span><span class="sxs-lookup"><span data-stu-id="b7d06-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="b7d06-122">Без фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="b7d06-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="b7d06-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="b7d06-123">0x00000006</span></span>  <br/> |<span data-ttu-id="b7d06-124">Фильтрация нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="b7d06-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="b7d06-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b7d06-125">0x00000003</span></span>  <br/> |<span data-ttu-id="b7d06-126">Высокая фильтрация нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="b7d06-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="b7d06-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="b7d06-127">0x80000000</span></span>  <br/> |<span data-ttu-id="b7d06-128">Только надежные списки</span><span class="sxs-lookup"><span data-stu-id="b7d06-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b7d06-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7d06-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7d06-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b7d06-130">Protocol specifications</span></span>

<span data-ttu-id="b7d06-131">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7d06-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7d06-132">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b7d06-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7d06-133">[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7d06-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7d06-134">Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b7d06-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7d06-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b7d06-135">Header files</span></span>

<span data-ttu-id="b7d06-136">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b7d06-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7d06-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b7d06-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7d06-138">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b7d06-138">Mapitags.h</span></span>
  
> <span data-ttu-id="b7d06-139">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b7d06-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7d06-140">См. также</span><span class="sxs-lookup"><span data-stu-id="b7d06-140">See also</span></span>



[<span data-ttu-id="b7d06-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b7d06-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7d06-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b7d06-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7d06-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b7d06-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7d06-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b7d06-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

