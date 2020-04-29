---
title: Каноническое свойство PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279631"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="5db7e-103">Каноническое свойство PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="5db7e-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="5db7e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5db7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5db7e-105">Содержит значение поля заголовка справки для многоцелевого почтового расширения в Интернете (MIME).</span><span class="sxs-lookup"><span data-stu-id="5db7e-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5db7e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5db7e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5db7e-107">PR_LIST_HELP, PR_LIST_HELP_A PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="5db7e-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="5db7e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5db7e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5db7e-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="5db7e-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="5db7e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5db7e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5db7e-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5db7e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5db7e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5db7e-112">Area:</span></span>  <br/> |<span data-ttu-id="5db7e-113">Разное</span><span class="sxs-lookup"><span data-stu-id="5db7e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5db7e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5db7e-114">Remarks</span></span>

<span data-ttu-id="5db7e-115">Чтобы создать поле заголовка списка справки, клиентам необходимо задать для свойства **PR_LIST_HELP** или связанного свойства нужное значение.</span><span class="sxs-lookup"><span data-stu-id="5db7e-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="5db7e-116">Модули записи MIME должны скопировать это значение в поле заголовка List – Help.</span><span class="sxs-lookup"><span data-stu-id="5db7e-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="5db7e-117">Чтобы задать значение этих свойств, связанных с сервером, клиенты MIME должны записать поля заголовков, как указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="5db7e-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="5db7e-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="5db7e-118">**Property**</span></span>|<span data-ttu-id="5db7e-119">**Имя основного поля заголовка**</span><span class="sxs-lookup"><span data-stu-id="5db7e-119">**Preferred header field name**</span></span>|<span data-ttu-id="5db7e-120">**Имя поля альтернативного заголовка**</span><span class="sxs-lookup"><span data-stu-id="5db7e-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5db7e-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="5db7e-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="5db7e-122">List – Справка</span><span class="sxs-lookup"><span data-stu-id="5db7e-122">List-Help</span></span>  <br/> |<span data-ttu-id="5db7e-123">Список "X" — Справка</span><span class="sxs-lookup"><span data-stu-id="5db7e-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5db7e-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5db7e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5db7e-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5db7e-125">Protocol specifications</span></span>

<span data-ttu-id="5db7e-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5db7e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5db7e-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5db7e-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5db7e-128">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5db7e-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5db7e-129">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="5db7e-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5db7e-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5db7e-130">Header files</span></span>

<span data-ttu-id="5db7e-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5db7e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5db7e-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5db7e-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5db7e-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5db7e-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5db7e-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5db7e-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5db7e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5db7e-135">See also</span></span>



[<span data-ttu-id="5db7e-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5db7e-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5db7e-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5db7e-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5db7e-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5db7e-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5db7e-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5db7e-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

