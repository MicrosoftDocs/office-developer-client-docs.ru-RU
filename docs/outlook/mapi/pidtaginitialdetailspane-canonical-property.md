---
title: Каноническое свойство PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346580"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="48d0f-103">Каноническое свойство PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="48d0f-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="48d0f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48d0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48d0f-105">Указывает страницу шаблона отображения для отображения в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="48d0f-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48d0f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="48d0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48d0f-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="48d0f-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="48d0f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="48d0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48d0f-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="48d0f-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="48d0f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="48d0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="48d0f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="48d0f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="48d0f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="48d0f-112">Area:</span></span>  <br/> |<span data-ttu-id="48d0f-113">Таблицы отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="48d0f-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48d0f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="48d0f-114">Remarks</span></span>

<span data-ttu-id="48d0f-115">Он должен присутствовать на всех объектах адресной книги на сервере интерфейса поставщика служб имени (NSPI) и иметь значение 0 (0).</span><span class="sxs-lookup"><span data-stu-id="48d0f-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="48d0f-116">Она не должна быть определена для любых объектов в автономной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="48d0f-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48d0f-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="48d0f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48d0f-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="48d0f-118">Protocol specifications</span></span>

<span data-ttu-id="48d0f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48d0f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48d0f-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="48d0f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48d0f-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48d0f-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48d0f-122">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48d0f-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48d0f-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="48d0f-123">Header files</span></span>

<span data-ttu-id="48d0f-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48d0f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="48d0f-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="48d0f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="48d0f-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48d0f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="48d0f-127">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="48d0f-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48d0f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="48d0f-128">See also</span></span>



[<span data-ttu-id="48d0f-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48d0f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48d0f-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48d0f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48d0f-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="48d0f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48d0f-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="48d0f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

