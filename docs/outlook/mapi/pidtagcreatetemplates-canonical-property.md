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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438185"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="04349-103">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="04349-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="04349-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04349-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04349-105">Содержит внедренный объект таблицы, содержащий идентификаторы записей шаблона диалоговых окной.</span><span class="sxs-lookup"><span data-stu-id="04349-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04349-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="04349-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04349-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="04349-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="04349-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="04349-108">Identifier:</span></span>  <br/> |<span data-ttu-id="04349-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="04349-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="04349-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="04349-110">Data type:</span></span>  <br/> |<span data-ttu-id="04349-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="04349-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="04349-112">Область:</span><span class="sxs-lookup"><span data-stu-id="04349-112">Area:</span></span>  <br/> |<span data-ttu-id="04349-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="04349-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04349-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="04349-114">Remarks</span></span>

<span data-ttu-id="04349-115">Чтобы узнать, какие объекты шаблона можно создать в контейнере, вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="04349-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="04349-116">Итоговый объект — это одноразовая таблица, которая предоставляет идентификаторы записей для всех шаблонов, которые можно создать в контейнере.</span><span class="sxs-lookup"><span data-stu-id="04349-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="04349-117">Чтобы создать объекты шаблона, вызовите метод **CreateEntry** объекта контейнера для значений столбца **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)из одноразовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="04349-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04349-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04349-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="04349-119">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="04349-119">Header files</span></span>

<span data-ttu-id="04349-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04349-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="04349-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="04349-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="04349-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="04349-122">Mapitags.h</span></span>
  
> <span data-ttu-id="04349-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="04349-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04349-124">См. также</span><span class="sxs-lookup"><span data-stu-id="04349-124">See also</span></span>



[<span data-ttu-id="04349-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="04349-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="04349-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="04349-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04349-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="04349-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04349-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="04349-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04349-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="04349-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

