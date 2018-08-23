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
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563361"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="8a3bd-103">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="8a3bd-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="8a3bd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a3bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a3bd-105">Содержит объект внедренных в таблице, который содержит идентификаторы записей шаблона поля диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8a3bd-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a3bd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a3bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a3bd-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="8a3bd-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="8a3bd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8a3bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a3bd-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="8a3bd-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="8a3bd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a3bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a3bd-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8a3bd-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8a3bd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8a3bd-112">Area:</span></span>  <br/> |<span data-ttu-id="8a3bd-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="8a3bd-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a3bd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a3bd-114">Remarks</span></span>

<span data-ttu-id="8a3bd-115">Чтобы узнать, какой шаблон объекты могут быть созданы в контейнере, вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на это свойство.</span><span class="sxs-lookup"><span data-stu-id="8a3bd-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="8a3bd-116">Полученный объект является таблицей одноразовых, задающей идентификаторы записей для всех шаблонов, которые можно создавать внутри контейнера.</span><span class="sxs-lookup"><span data-stu-id="8a3bd-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="8a3bd-117">Для создания объекта шаблона, вызовите метод **CreateEntry** объекта-контейнера на значения столбцов **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) в одноразовых TABLE.</span><span class="sxs-lookup"><span data-stu-id="8a3bd-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a3bd-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a3bd-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a3bd-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8a3bd-119">Header files</span></span>

<span data-ttu-id="8a3bd-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a3bd-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a3bd-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a3bd-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a3bd-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a3bd-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8a3bd-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="8a3bd-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a3bd-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8a3bd-124">See also</span></span>



[<span data-ttu-id="8a3bd-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="8a3bd-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="8a3bd-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3bd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a3bd-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3bd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a3bd-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a3bd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a3bd-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8a3bd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

