---
title: Каноническое свойство PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279659"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="9b598-103">Каноническое свойство PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="9b598-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="9b598-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b598-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b598-105">Содержит значение поля заголовка List-Subscribe-почтовые расширения для многоцелевого протокола (MIME).</span><span class="sxs-lookup"><span data-stu-id="9b598-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b598-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9b598-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b598-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="9b598-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="9b598-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9b598-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b598-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="9b598-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="9b598-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9b598-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b598-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b598-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b598-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9b598-112">Area:</span></span>  <br/> |<span data-ttu-id="9b598-113">Разное</span><span class="sxs-lookup"><span data-stu-id="9b598-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b598-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b598-114">Remarks</span></span>

<span data-ttu-id="9b598-115">Для создания поля заголовка List – Subscribe клиенты должны присвоить значениям этих свойств нужное значение.</span><span class="sxs-lookup"><span data-stu-id="9b598-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="9b598-116">Записи MIME должны копировать значения этих свойств в поле заголовка List – Subscribe.</span><span class="sxs-lookup"><span data-stu-id="9b598-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="9b598-117">Чтобы задать значения свойств, связанных с сервером, клиенты MIME должны записать поля заголовков, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9b598-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="9b598-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="9b598-118">**Property**</span></span>|<span data-ttu-id="9b598-119">**Имя основного поля заголовка**</span><span class="sxs-lookup"><span data-stu-id="9b598-119">**Preferred header field name**</span></span>|<span data-ttu-id="9b598-120">**Имя поля альтернативного заголовка**</span><span class="sxs-lookup"><span data-stu-id="9b598-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b598-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="9b598-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="9b598-122">List – Subscribe</span><span class="sxs-lookup"><span data-stu-id="9b598-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="9b598-123">X – List — Subscribe</span><span class="sxs-lookup"><span data-stu-id="9b598-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9b598-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9b598-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b598-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9b598-125">Protocol specifications</span></span>

<span data-ttu-id="9b598-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b598-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b598-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9b598-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b598-128">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b598-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b598-129">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b598-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b598-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9b598-130">Header files</span></span>

<span data-ttu-id="9b598-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9b598-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b598-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9b598-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b598-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9b598-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9b598-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="9b598-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b598-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9b598-135">See also</span></span>



[<span data-ttu-id="9b598-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9b598-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b598-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9b598-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b598-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9b598-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b598-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9b598-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

