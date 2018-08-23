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
ms.openlocfilehash: 91eb93c9cf3afcecef698e27791c06831c13624d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589100"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="deeb0-103">Каноническое свойство PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="deeb0-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="deeb0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deeb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deeb0-105">Содержит значение поля заголовка [RFC3282] Content-Base.</span><span class="sxs-lookup"><span data-stu-id="deeb0-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="deeb0-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="deeb0-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="deeb0-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="deeb0-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="deeb0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="deeb0-108">Property set:</span></span>  <br/> |<span data-ttu-id="deeb0-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="deeb0-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="deeb0-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="deeb0-110">Property name:</span></span>  <br/> |<span data-ttu-id="deeb0-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="deeb0-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="deeb0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="deeb0-112">Data type:</span></span>  <br/> |<span data-ttu-id="deeb0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="deeb0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="deeb0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="deeb0-114">Area:</span></span>  <br/> |<span data-ttu-id="deeb0-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="deeb0-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="deeb0-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="deeb0-116">Remarks</span></span>

<span data-ttu-id="deeb0-117">Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) необходимо создать нужное значение в поле Заголовок Content-Base в сущности MIME, которая сопоставлена с текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="deeb0-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="deeb0-118">Читатели MIME необходимо скопировать значение в поле Заголовок Content-Base в сущности MIME значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="deeb0-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="deeb0-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="deeb0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="deeb0-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="deeb0-120">Protocol specifications</span></span>

<span data-ttu-id="deeb0-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deeb0-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deeb0-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="deeb0-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="deeb0-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deeb0-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deeb0-124">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="deeb0-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="deeb0-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="deeb0-125">Header files</span></span>

<span data-ttu-id="deeb0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="deeb0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="deeb0-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="deeb0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="deeb0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="deeb0-128">See also</span></span>



[<span data-ttu-id="deeb0-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="deeb0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="deeb0-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="deeb0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="deeb0-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="deeb0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="deeb0-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="deeb0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

