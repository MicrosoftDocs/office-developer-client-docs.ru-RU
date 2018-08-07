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
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811023"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="807f3-103">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="807f3-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="807f3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="807f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="807f3-105">Содержит объект внедренных в таблице, который содержит идентификаторы записей шаблона поля диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="807f3-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="807f3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="807f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="807f3-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="807f3-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="807f3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="807f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="807f3-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="807f3-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="807f3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="807f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="807f3-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="807f3-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="807f3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="807f3-112">Area:</span></span>  <br/> |<span data-ttu-id="807f3-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="807f3-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="807f3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="807f3-114">Remarks</span></span>

<span data-ttu-id="807f3-115">Чтобы узнать, какой шаблон объекты могут быть созданы в контейнере, вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на это свойство.</span><span class="sxs-lookup"><span data-stu-id="807f3-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="807f3-116">Полученный объект является таблицей одноразовых, задающей идентификаторы записей для всех шаблонов, которые можно создавать внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="807f3-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="807f3-117">Для создания объекта шаблона, вызовите метод **CreateEntry** объекта-контейнера на значения столбцов **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) в одноразовых TABLE.</span><span class="sxs-lookup"><span data-stu-id="807f3-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="807f3-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="807f3-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="807f3-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="807f3-119">Header files</span></span>

<span data-ttu-id="807f3-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="807f3-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="807f3-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="807f3-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="807f3-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="807f3-122">Mapitags.h</span></span>
  
> <span data-ttu-id="807f3-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="807f3-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="807f3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="807f3-124">See also</span></span>



[<span data-ttu-id="807f3-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="807f3-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="807f3-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="807f3-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="807f3-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="807f3-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="807f3-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="807f3-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="807f3-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="807f3-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

