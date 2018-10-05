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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384544"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="ecbf1-103">Каноническое свойство PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="ecbf1-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="ecbf1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecbf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecbf1-105">Содержит значение поля Заголовок Content-Class [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="ecbf1-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecbf1-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="ecbf1-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ecbf1-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ecbf1-107">None</span></span>  <br/> |
|<span data-ttu-id="ecbf1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ecbf1-108">Property set:</span></span>  <br/> |<span data-ttu-id="ecbf1-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ecbf1-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="ecbf1-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="ecbf1-110">Property name:</span></span>  <br/> |<span data-ttu-id="ecbf1-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="ecbf1-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="ecbf1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ecbf1-112">Data type:</span></span>  <br/> |<span data-ttu-id="ecbf1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecbf1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ecbf1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ecbf1-114">Area:</span></span>  <br/> |<span data-ttu-id="ecbf1-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="ecbf1-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecbf1-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ecbf1-116">Remarks</span></span>

<span data-ttu-id="ecbf1-117">Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) необходимо создать поле Заголовок Content-Class с нужное значение.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="ecbf1-118">Читатели MIME необходимо скопировать значение в поле Заголовок Content-Class значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ecbf1-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ecbf1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecbf1-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ecbf1-120">Protocol specifications</span></span>

<span data-ttu-id="ecbf1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecbf1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecbf1-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecbf1-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecbf1-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecbf1-124">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ecbf1-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecbf1-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecbf1-126">Задает свойства управляемый правами закодированный сообщений.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecbf1-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ecbf1-127">Header files</span></span>

<span data-ttu-id="ecbf1-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecbf1-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecbf1-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecbf1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ecbf1-130">See also</span></span>



[<span data-ttu-id="ecbf1-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecbf1-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecbf1-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ecbf1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecbf1-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ecbf1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

