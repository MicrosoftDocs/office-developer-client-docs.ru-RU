---
title: Каноническое свойство PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344977"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="8c44f-103">Каноническое свойство PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="8c44f-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="8c44f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c44f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c44f-105">Задает список категорий для элемента.</span><span class="sxs-lookup"><span data-stu-id="8c44f-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c44f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8c44f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c44f-107">Диспидкатегориес</span><span class="sxs-lookup"><span data-stu-id="8c44f-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="8c44f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8c44f-108">Property set:</span></span>  <br/> |<span data-ttu-id="8c44f-109">ПС_ПУБЛИК_СТРИНГС</span><span class="sxs-lookup"><span data-stu-id="8c44f-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="8c44f-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="8c44f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8c44f-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="8c44f-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="8c44f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8c44f-112">Data type:</span></span>  <br/> |<span data-ttu-id="8c44f-113">ПТ_МВ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="8c44f-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8c44f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8c44f-114">Area:</span></span>  <br/> |<span data-ttu-id="8c44f-115">Распространенная</span><span class="sxs-lookup"><span data-stu-id="8c44f-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c44f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c44f-116">Remarks</span></span>

<span data-ttu-id="8c44f-117">Чтобы создать поле заголовка ключевых слов, клиенты должны присвоить значение этого свойства желаемым значениям.</span><span class="sxs-lookup"><span data-stu-id="8c44f-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="8c44f-118">Это свойство содержит несколько строк; Каждая категория должна быть сопоставлена с одним ключевым словом.</span><span class="sxs-lookup"><span data-stu-id="8c44f-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="8c44f-119">Средства записи MIME должны копировать каждое значение этого свойства в отдельное ключевое слово в поле заголовка ключевых слов с запятой (U + 002C) и пространством (U + 0020), разделяющее каждое ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="8c44f-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="8c44f-120">Записи MIME могут удалять это свойство, а не копировать его в поле заголовка ключевых слов, чтобы избежать конфликтов между различными наборами категорий в разных организациях.</span><span class="sxs-lookup"><span data-stu-id="8c44f-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c44f-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8c44f-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c44f-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8c44f-122">Protocol specifications</span></span>

<span data-ttu-id="8c44f-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c44f-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c44f-124">Предоставляет определение набора свойств и ссылки на соответствующие спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8c44f-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c44f-125">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c44f-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c44f-126">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c44f-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c44f-127">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8c44f-127">Header files</span></span>

<span data-ttu-id="8c44f-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8c44f-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c44f-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8c44f-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c44f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8c44f-130">See also</span></span>



[<span data-ttu-id="8c44f-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8c44f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c44f-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8c44f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c44f-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8c44f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c44f-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8c44f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

