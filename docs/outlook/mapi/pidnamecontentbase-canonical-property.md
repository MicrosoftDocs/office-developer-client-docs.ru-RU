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
ms.openlocfilehash: 21469b944bb2ce5db0576e40012335d89d48cb49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810736"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="81839-103">Каноническое свойство PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="81839-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="81839-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81839-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81839-105">Содержит значение поля заголовка [RFC3282] Content-Base.</span><span class="sxs-lookup"><span data-stu-id="81839-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81839-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="81839-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="81839-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="81839-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="81839-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="81839-108">Property set:</span></span>  <br/> |<span data-ttu-id="81839-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="81839-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="81839-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="81839-110">Property name:</span></span>  <br/> |<span data-ttu-id="81839-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="81839-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="81839-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="81839-112">Data type:</span></span>  <br/> |<span data-ttu-id="81839-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="81839-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="81839-114">Область:</span><span class="sxs-lookup"><span data-stu-id="81839-114">Area:</span></span>  <br/> |<span data-ttu-id="81839-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="81839-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81839-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="81839-116">Remarks</span></span>

<span data-ttu-id="81839-117">Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) необходимо создать нужное значение в поле Заголовок Content-Base в сущности MIME, которая сопоставлена с текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="81839-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="81839-118">Читатели MIME необходимо скопировать значение в поле Заголовок Content-Base в сущности MIME значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="81839-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="81839-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="81839-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81839-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="81839-120">Protocol specifications</span></span>

<span data-ttu-id="81839-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81839-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81839-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="81839-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81839-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81839-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81839-124">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="81839-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81839-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="81839-125">Header files</span></span>

<span data-ttu-id="81839-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81839-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="81839-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="81839-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81839-128">См. также</span><span class="sxs-lookup"><span data-stu-id="81839-128">See also</span></span>



[<span data-ttu-id="81839-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="81839-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81839-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="81839-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81839-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="81839-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81839-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="81839-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

