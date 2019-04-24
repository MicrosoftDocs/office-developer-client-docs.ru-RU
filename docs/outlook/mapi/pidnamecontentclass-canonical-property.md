---
title: Каноническое свойство PidNameContentClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356352"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="9d4c9-103">Каноническое свойство PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="9d4c9-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="9d4c9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d4c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d4c9-105">Содержит значение поля заголовка Content – class [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="9d4c9-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d4c9-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="9d4c9-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="9d4c9-107">Нет</span><span class="sxs-lookup"><span data-stu-id="9d4c9-107">None</span></span>  <br/> |
|<span data-ttu-id="9d4c9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9d4c9-108">Property set:</span></span>  <br/> |<span data-ttu-id="9d4c9-109">ПС_ИНТЕРНЕТ_ХЕАДЕРС</span><span class="sxs-lookup"><span data-stu-id="9d4c9-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="9d4c9-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="9d4c9-110">Property name:</span></span>  <br/> |<span data-ttu-id="9d4c9-111">Content – class</span><span class="sxs-lookup"><span data-stu-id="9d4c9-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="9d4c9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9d4c9-112">Data type:</span></span>  <br/> |<span data-ttu-id="9d4c9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d4c9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9d4c9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9d4c9-114">Area:</span></span>  <br/> |<span data-ttu-id="9d4c9-115">Email</span><span class="sxs-lookup"><span data-stu-id="9d4c9-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d4c9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d4c9-116">Remarks</span></span>

<span data-ttu-id="9d4c9-117">Чтобы задать значение этого свойства, клиенты с многоцелевыми расширениями Интернет-сообщений (MIME) должны записать поле заголовка Content-class с требуемым значением.</span><span class="sxs-lookup"><span data-stu-id="9d4c9-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="9d4c9-118">Считыватели MIME должны скопировать значение поля заголовка Content – class в значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="9d4c9-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d4c9-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9d4c9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d4c9-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9d4c9-120">Protocol specifications</span></span>

<span data-ttu-id="9d4c9-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d4c9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d4c9-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9d4c9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d4c9-123">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d4c9-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d4c9-124">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d4c9-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="9d4c9-125">[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d4c9-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d4c9-126">Задает свойства сообщений, закодированных с помощью управления правами.</span><span class="sxs-lookup"><span data-stu-id="9d4c9-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d4c9-127">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9d4c9-127">Header files</span></span>

<span data-ttu-id="9d4c9-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9d4c9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d4c9-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9d4c9-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d4c9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9d4c9-130">See also</span></span>



[<span data-ttu-id="9d4c9-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9d4c9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d4c9-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9d4c9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d4c9-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9d4c9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d4c9-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9d4c9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

