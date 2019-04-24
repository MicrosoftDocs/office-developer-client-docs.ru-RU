---
title: Каноническое свойство PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269939"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="2b645-103">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="2b645-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="2b645-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b645-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b645-105">Содержит объект внедренной таблицы, который содержит идентификаторы элементов шаблона диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2b645-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b645-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2b645-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b645-107">ПР_КРЕАТЕ_ТЕМПЛАТЕС</span><span class="sxs-lookup"><span data-stu-id="2b645-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="2b645-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2b645-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b645-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="2b645-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="2b645-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2b645-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b645-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="2b645-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="2b645-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2b645-112">Area:</span></span>  <br/> |<span data-ttu-id="2b645-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="2b645-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b645-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2b645-114">Remarks</span></span>

<span data-ttu-id="2b645-115">Чтобы узнать, какие объекты шаблонов можно создать в контейнере, вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="2b645-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="2b645-116">Полученный объект является одноразовой таблицей, которая предоставляет идентификаторы записей для всех шаблонов, которые можно создать в контейнере.</span><span class="sxs-lookup"><span data-stu-id="2b645-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="2b645-117">Чтобы создать объекты шаблона, вызовите метод **креатинтри** объекта Container для значений столбца **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из таблицы с отправителями.</span><span class="sxs-lookup"><span data-stu-id="2b645-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b645-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b645-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2b645-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="2b645-119">Header files</span></span>

<span data-ttu-id="2b645-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2b645-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b645-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2b645-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b645-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="2b645-122">Mapitags.h</span></span>
  
> <span data-ttu-id="2b645-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="2b645-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b645-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2b645-124">See also</span></span>



[<span data-ttu-id="2b645-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="2b645-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="2b645-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2b645-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b645-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2b645-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b645-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2b645-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b645-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2b645-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

