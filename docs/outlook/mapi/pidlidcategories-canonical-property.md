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
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810217"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="25d67-103">Каноническое свойство PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="25d67-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="25d67-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25d67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25d67-105">Указывает список категорий для элемента.</span><span class="sxs-lookup"><span data-stu-id="25d67-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25d67-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="25d67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25d67-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="25d67-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="25d67-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="25d67-108">Property set:</span></span>  <br/> |<span data-ttu-id="25d67-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="25d67-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="25d67-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="25d67-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25d67-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="25d67-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="25d67-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="25d67-112">Data type:</span></span>  <br/> |<span data-ttu-id="25d67-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25d67-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25d67-114">Область:</span><span class="sxs-lookup"><span data-stu-id="25d67-114">Area:</span></span>  <br/> |<span data-ttu-id="25d67-115">Common</span><span class="sxs-lookup"><span data-stu-id="25d67-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25d67-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="25d67-116">Remarks</span></span>

<span data-ttu-id="25d67-117">Чтобы создать поле заголовка ключевые слова, клиенты необходимо присвоить значение этого свойства необходимые значения.</span><span class="sxs-lookup"><span data-stu-id="25d67-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="25d67-118">Это свойство имеет несколько строк; каждой категории должна быть сопоставлена с одного ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="25d67-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="25d67-119">Записи Multipurpose Internet Mail Extensions (MIME) следует скопировать каждого подменю значение этого свойства для отдельных ключевое слово в поле Заголовок ключевые слова с запятой (U + 002 C) и разделения пространства (U + 0020) каждого ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="25d67-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="25d67-120">Записи MIME может удалить это свойство вместо копирования поле заголовка ключевые слова, чтобы избежать конфликтов между различными наборами категорий в различных организациях.</span><span class="sxs-lookup"><span data-stu-id="25d67-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25d67-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25d67-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25d67-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="25d67-122">Protocol specifications</span></span>

<span data-ttu-id="25d67-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25d67-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25d67-124">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="25d67-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25d67-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25d67-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25d67-126">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="25d67-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25d67-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="25d67-127">Header files</span></span>

<span data-ttu-id="25d67-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25d67-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="25d67-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="25d67-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25d67-130">См. также</span><span class="sxs-lookup"><span data-stu-id="25d67-130">See also</span></span>



[<span data-ttu-id="25d67-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25d67-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25d67-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="25d67-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25d67-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="25d67-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25d67-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="25d67-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

