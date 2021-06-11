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
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="62f0a-103">Каноническое свойство PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="62f0a-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="62f0a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62f0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62f0a-105">Содержит значение поля поля заглавной области Xref [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="62f0a-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62f0a-106">Дружественные имена:</span><span class="sxs-lookup"><span data-stu-id="62f0a-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="62f0a-107">Нет</span><span class="sxs-lookup"><span data-stu-id="62f0a-107">None</span></span>  <br/> |
|<span data-ttu-id="62f0a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="62f0a-108">Property set:</span></span>  <br/> |<span data-ttu-id="62f0a-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="62f0a-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="62f0a-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="62f0a-110">Property name:</span></span>  <br/> |<span data-ttu-id="62f0a-111">Xref</span><span class="sxs-lookup"><span data-stu-id="62f0a-111">Xref</span></span>  <br/> |
|<span data-ttu-id="62f0a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="62f0a-112">Data type:</span></span>  <br/> |<span data-ttu-id="62f0a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="62f0a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="62f0a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="62f0a-114">Area:</span></span>  <br/> |<span data-ttu-id="62f0a-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="62f0a-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62f0a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="62f0a-116">Remarks</span></span>

<span data-ttu-id="62f0a-117">Чтобы задать значение этого свойства, клиенты multipurpose Internet Message Extensions (MIME) должны написать нужное значение в поле загон XRef.</span><span class="sxs-lookup"><span data-stu-id="62f0a-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="62f0a-118">Читатели MIME должны скопировать значение поля заглавного поля XRef к значению этого свойства.</span><span class="sxs-lookup"><span data-stu-id="62f0a-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62f0a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="62f0a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62f0a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="62f0a-120">Protocol specifications</span></span>

<span data-ttu-id="62f0a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62f0a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62f0a-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="62f0a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62f0a-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62f0a-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62f0a-124">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="62f0a-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62f0a-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="62f0a-125">Header files</span></span>

<span data-ttu-id="62f0a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62f0a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="62f0a-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="62f0a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62f0a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="62f0a-128">See also</span></span>



[<span data-ttu-id="62f0a-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62f0a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62f0a-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="62f0a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62f0a-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="62f0a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62f0a-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="62f0a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

