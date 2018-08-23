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
ms.openlocfilehash: 5daf8c1ee249cfc7fb1bc1ffb6dfc68b400fe953
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571131"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="5d336-103">Каноническое свойство PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="5d336-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="5d336-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d336-105">Содержит значение поля заголовка перекрестные ссылки на модель [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="5d336-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d336-106">Понятные имена:</span><span class="sxs-lookup"><span data-stu-id="5d336-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="5d336-107">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="5d336-107">None</span></span>  <br/> |
|<span data-ttu-id="5d336-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5d336-108">Property set:</span></span>  <br/> |<span data-ttu-id="5d336-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5d336-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="5d336-110">Имя свойства:</span><span class="sxs-lookup"><span data-stu-id="5d336-110">Property name:</span></span>  <br/> |<span data-ttu-id="5d336-111">Перекрестные ссылки на модель</span><span class="sxs-lookup"><span data-stu-id="5d336-111">Xref</span></span>  <br/> |
|<span data-ttu-id="5d336-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5d336-112">Data type:</span></span>  <br/> |<span data-ttu-id="5d336-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5d336-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5d336-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5d336-114">Area:</span></span>  <br/> |<span data-ttu-id="5d336-115">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="5d336-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d336-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5d336-116">Remarks</span></span>

<span data-ttu-id="5d336-117">Чтобы задать значение этого свойства, клиенты сообщение расширения MIME (Multipurpose Internet) необходимо создать нужное значение в поле Заголовок перекрестные ссылки на модель.</span><span class="sxs-lookup"><span data-stu-id="5d336-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="5d336-118">Читатели MIME необходимо скопировать значение поля заголовка перекрестные ссылки на модель значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="5d336-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d336-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5d336-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d336-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5d336-120">Protocol specifications</span></span>

<span data-ttu-id="5d336-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d336-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d336-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5d336-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d336-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d336-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d336-124">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="5d336-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d336-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5d336-125">Header files</span></span>

<span data-ttu-id="5d336-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d336-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d336-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5d336-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d336-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5d336-128">See also</span></span>



[<span data-ttu-id="5d336-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5d336-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d336-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5d336-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d336-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5d336-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d336-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5d336-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

