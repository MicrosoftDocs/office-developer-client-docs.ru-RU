---
title: Каноническое свойство PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331502"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="d2fdf-103">Каноническое свойство PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="d2fdf-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="d2fdf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2fdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2fdf-105">Содержит значение поля загона [RFC3282] Content-Base.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2fdf-106">Дружелюбные имена:</span><span class="sxs-lookup"><span data-stu-id="d2fdf-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="d2fdf-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="d2fdf-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="d2fdf-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d2fdf-108">Property set:</span></span>  <br/> |<span data-ttu-id="d2fdf-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="d2fdf-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="d2fdf-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="d2fdf-110">Property name:</span></span>  <br/> |<span data-ttu-id="d2fdf-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="d2fdf-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="d2fdf-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d2fdf-112">Data type:</span></span>  <br/> |<span data-ttu-id="d2fdf-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2fdf-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d2fdf-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d2fdf-114">Area:</span></span>  <br/> |<span data-ttu-id="d2fdf-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="d2fdf-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2fdf-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2fdf-116">Remarks</span></span>

<span data-ttu-id="d2fdf-117">Чтобы установить значение этого свойства, клиенты MIME должны записать нужное значение в поле заголовщика Content-Base в объекте MIME, соповедуемом с текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="d2fdf-118">Читатели MIME должны скопировать значение поля загона Content-Base для такого объекта MIME в значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d2fdf-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d2fdf-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2fdf-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d2fdf-120">Protocol specifications</span></span>

<span data-ttu-id="d2fdf-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2fdf-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2fdf-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2fdf-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2fdf-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2fdf-124">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2fdf-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="d2fdf-125">Header files</span></span>

<span data-ttu-id="d2fdf-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2fdf-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2fdf-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2fdf-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d2fdf-128">See also</span></span>



[<span data-ttu-id="d2fdf-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fdf-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2fdf-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fdf-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2fdf-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fdf-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2fdf-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d2fdf-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

