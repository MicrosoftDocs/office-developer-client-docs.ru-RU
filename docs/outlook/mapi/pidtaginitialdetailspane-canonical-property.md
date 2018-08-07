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
ms.openlocfilehash: 884bbad509e459d4f329e6468dd99124cec6c7d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811221"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="22494-103">Каноническое свойство PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="22494-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="22494-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22494-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22494-105">Указывает страницу шаблона для отображения для отображения первоначального.</span><span class="sxs-lookup"><span data-stu-id="22494-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22494-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="22494-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22494-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="22494-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="22494-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="22494-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22494-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="22494-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="22494-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="22494-110">Data type:</span></span>  <br/> |<span data-ttu-id="22494-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22494-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22494-112">Область:</span><span class="sxs-lookup"><span data-stu-id="22494-112">Area:</span></span>  <br/> |<span data-ttu-id="22494-113">Отображать таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="22494-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22494-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="22494-114">Remarks</span></span>

<span data-ttu-id="22494-115">Должны быть установлены на все объекты адресной книги на сервере интерфейса поставщика имя службы (NSPI) и должен иметь значение нуль (0).</span><span class="sxs-lookup"><span data-stu-id="22494-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="22494-116">Он не должно быть задано для всех объектов в автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="22494-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22494-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="22494-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22494-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="22494-118">Protocol specifications</span></span>

<span data-ttu-id="22494-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22494-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22494-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="22494-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22494-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22494-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22494-122">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22494-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22494-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="22494-123">Header files</span></span>

<span data-ttu-id="22494-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22494-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="22494-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="22494-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="22494-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22494-126">Mapitags.h</span></span>
  
> <span data-ttu-id="22494-127">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="22494-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22494-128">См. также</span><span class="sxs-lookup"><span data-stu-id="22494-128">See also</span></span>



[<span data-ttu-id="22494-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22494-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22494-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22494-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22494-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="22494-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22494-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="22494-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

