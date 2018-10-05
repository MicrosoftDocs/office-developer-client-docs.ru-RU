---
title: Каноническое свойство PidLidWhere
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390564"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="13ec2-103">Каноническое свойство PidLidWhere</span><span class="sxs-lookup"><span data-stu-id="13ec2-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="13ec2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13ec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13ec2-105">Указывает расположение события.</span><span class="sxs-lookup"><span data-stu-id="13ec2-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13ec2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="13ec2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13ec2-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="13ec2-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="13ec2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="13ec2-108">Property set:</span></span>  <br/> |<span data-ttu-id="13ec2-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="13ec2-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="13ec2-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="13ec2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13ec2-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="13ec2-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="13ec2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="13ec2-112">Data type:</span></span>  <br/> |<span data-ttu-id="13ec2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13ec2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13ec2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="13ec2-114">Area:</span></span>  <br/> |<span data-ttu-id="13ec2-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="13ec2-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13ec2-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="13ec2-116">Remarks</span></span>

<span data-ttu-id="13ec2-117">Значение этого свойства должны совпадать с значение свойства **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) из связанной собрания.</span><span class="sxs-lookup"><span data-stu-id="13ec2-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13ec2-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13ec2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13ec2-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="13ec2-119">Protocol specifications</span></span>

<span data-ttu-id="13ec2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13ec2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13ec2-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13ec2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13ec2-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13ec2-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13ec2-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="13ec2-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13ec2-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="13ec2-124">Header files</span></span>

<span data-ttu-id="13ec2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13ec2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="13ec2-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="13ec2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13ec2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="13ec2-127">See also</span></span>



[<span data-ttu-id="13ec2-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13ec2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13ec2-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13ec2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13ec2-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="13ec2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13ec2-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="13ec2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

