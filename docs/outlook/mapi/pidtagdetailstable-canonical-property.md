---
title: Каноническое свойство PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360839"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="e4f84-103">Каноническое свойство PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="e4f84-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="e4f84-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4f84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4f84-105">Содержит внедренный объект таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="e4f84-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4f84-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e4f84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4f84-107">ПР_ДЕТАИЛС_ТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="e4f84-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="e4f84-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e4f84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4f84-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="e4f84-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="e4f84-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e4f84-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4f84-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="e4f84-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="e4f84-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e4f84-112">Area:</span></span>  <br/> |<span data-ttu-id="e4f84-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="e4f84-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4f84-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4f84-114">Remarks</span></span>

<span data-ttu-id="e4f84-115">При передаче этого свойства методу [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для объекта возвращается интерфейс [IMAPITable](imapitableiunknown.md) , позволяющий создать таблицу отображения.</span><span class="sxs-lookup"><span data-stu-id="e4f84-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="e4f84-116">MAPI использует эту таблицу для отображения страниц свойств для объекта адресной книги в ответ на вызов [IAddrBook::D етаилс](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f84-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e4f84-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e4f84-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e4f84-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="e4f84-118">Header files</span></span>

<span data-ttu-id="e4f84-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e4f84-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4f84-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e4f84-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4f84-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="e4f84-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e4f84-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="e4f84-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4f84-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e4f84-123">See also</span></span>



[<span data-ttu-id="e4f84-124">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="e4f84-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="e4f84-125">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="e4f84-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="e4f84-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e4f84-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4f84-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e4f84-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4f84-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e4f84-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4f84-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e4f84-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

