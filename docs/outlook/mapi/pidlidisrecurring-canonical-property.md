---
title: Каноническое свойство PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315437"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="8ec4b-103">Каноническое свойство PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="8ec4b-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="8ec4b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ec4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ec4b-105">Указывает, связан ли объект с повторяющимся набором.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ec4b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ec4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ec4b-107">ЛИД_ИС_РЕКУРРИНГ</span><span class="sxs-lookup"><span data-stu-id="8ec4b-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="8ec4b-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8ec4b-108">Property set:</span></span>  <br/> |<span data-ttu-id="8ec4b-109">Псетид_митинг</span><span class="sxs-lookup"><span data-stu-id="8ec4b-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="8ec4b-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="8ec4b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8ec4b-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8ec4b-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="8ec4b-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ec4b-112">Data type:</span></span>  <br/> |<span data-ttu-id="8ec4b-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8ec4b-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8ec4b-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8ec4b-114">Area:</span></span>  <br/> |<span data-ttu-id="8ec4b-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="8ec4b-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ec4b-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ec4b-116">Remarks</span></span>

<span data-ttu-id="8ec4b-117">Значение TRUE указывает, что объект представляет либо повторяющийся ряд, либо исключение (включая потерянный экземпляр).</span><span class="sxs-lookup"><span data-stu-id="8ec4b-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="8ec4b-118">Значение FALSE или отсутствие этого свойства указывает на то, что объект представляет один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="8ec4b-119">Обратите внимание на разницу между этим свойством и свойством **пр_рекурринг** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8ec4b-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8ec4b-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ec4b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ec4b-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8ec4b-121">Protocol specifications</span></span>

<span data-ttu-id="8ec4b-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ec4b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ec4b-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ec4b-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ec4b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ec4b-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ec4b-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8ec4b-126">Header files</span></span>

<span data-ttu-id="8ec4b-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8ec4b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ec4b-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ec4b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ec4b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="8ec4b-129">See also</span></span>



[<span data-ttu-id="8ec4b-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ec4b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ec4b-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8ec4b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ec4b-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ec4b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ec4b-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ec4b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

