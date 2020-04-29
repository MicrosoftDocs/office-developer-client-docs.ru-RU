---
title: Каноническое свойство PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331446"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="8b273-103">Каноническое свойство PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="8b273-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="8b273-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b273-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b273-105">Содержит значение поля заголовка Ксреф [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="8b273-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b273-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="8b273-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="8b273-107">Нет</span><span class="sxs-lookup"><span data-stu-id="8b273-107">None</span></span>  <br/> |
|<span data-ttu-id="8b273-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8b273-108">Property set:</span></span>  <br/> |<span data-ttu-id="8b273-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="8b273-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="8b273-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="8b273-110">Property name:</span></span>  <br/> |<span data-ttu-id="8b273-111">ксреф</span><span class="sxs-lookup"><span data-stu-id="8b273-111">Xref</span></span>  <br/> |
|<span data-ttu-id="8b273-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8b273-112">Data type:</span></span>  <br/> |<span data-ttu-id="8b273-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8b273-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8b273-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8b273-114">Area:</span></span>  <br/> |<span data-ttu-id="8b273-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="8b273-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b273-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b273-116">Remarks</span></span>

<span data-ttu-id="8b273-117">Чтобы задать значение этого свойства, клиенты с многоцелевыми расширениями Интернет-сообщений (MIME) должны записать нужное значение в поле заголовка Ксреф.</span><span class="sxs-lookup"><span data-stu-id="8b273-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="8b273-118">Считыватели MIME должны скопировать значение поля заголовка Ксреф в значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8b273-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b273-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8b273-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b273-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8b273-120">Protocol specifications</span></span>

<span data-ttu-id="8b273-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b273-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b273-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8b273-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b273-123">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b273-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b273-124">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="8b273-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b273-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8b273-125">Header files</span></span>

<span data-ttu-id="8b273-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8b273-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b273-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8b273-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b273-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8b273-128">See also</span></span>



[<span data-ttu-id="8b273-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8b273-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b273-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8b273-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b273-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8b273-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b273-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8b273-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

