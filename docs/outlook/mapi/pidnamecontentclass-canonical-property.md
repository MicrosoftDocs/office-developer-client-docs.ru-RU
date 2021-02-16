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
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="9406e-103">Каноническое свойство PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="9406e-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="9406e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9406e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9406e-105">Содержит значение поля загола [RFC3282] Content-Class.</span><span class="sxs-lookup"><span data-stu-id="9406e-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9406e-106">Дружелюбные имена:</span><span class="sxs-lookup"><span data-stu-id="9406e-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="9406e-107">Нет</span><span class="sxs-lookup"><span data-stu-id="9406e-107">None</span></span>  <br/> |
|<span data-ttu-id="9406e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9406e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9406e-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="9406e-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="9406e-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="9406e-110">Property name:</span></span>  <br/> |<span data-ttu-id="9406e-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="9406e-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="9406e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9406e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9406e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9406e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9406e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9406e-114">Area:</span></span>  <br/> |<span data-ttu-id="9406e-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="9406e-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9406e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9406e-116">Remarks</span></span>

<span data-ttu-id="9406e-117">Чтобы установить значение этого свойства, клиенты MIME должны написать поле загона content-Class с нужным значением.</span><span class="sxs-lookup"><span data-stu-id="9406e-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="9406e-118">Читатели MIME должны скопировать значение поля загона Content-Class в значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="9406e-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9406e-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9406e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9406e-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9406e-120">Protocol specifications</span></span>

<span data-ttu-id="9406e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9406e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9406e-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="9406e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9406e-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9406e-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9406e-124">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="9406e-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="9406e-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9406e-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9406e-126">Указывает свойства сообщений в кодированной кодировки с управлением правами.</span><span class="sxs-lookup"><span data-stu-id="9406e-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9406e-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="9406e-127">Header files</span></span>

<span data-ttu-id="9406e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9406e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9406e-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9406e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9406e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9406e-130">See also</span></span>



[<span data-ttu-id="9406e-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9406e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9406e-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9406e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9406e-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9406e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9406e-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9406e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

