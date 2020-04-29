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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419256"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="793e8-103">Каноническое свойство PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="793e8-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="793e8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="793e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="793e8-105">Содержит внедренный объект таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="793e8-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="793e8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="793e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="793e8-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="793e8-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="793e8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="793e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="793e8-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="793e8-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="793e8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="793e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="793e8-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="793e8-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="793e8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="793e8-112">Area:</span></span>  <br/> |<span data-ttu-id="793e8-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="793e8-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="793e8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="793e8-114">Remarks</span></span>

<span data-ttu-id="793e8-115">При передаче этого свойства методу [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для объекта возвращается интерфейс [IMAPITable](imapitableiunknown.md) , позволяющий создать таблицу отображения.</span><span class="sxs-lookup"><span data-stu-id="793e8-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="793e8-116">MAPI использует эту таблицу для отображения страниц свойств для объекта адресной книги в ответ на вызов [IAddrBook::D етаилс](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="793e8-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="793e8-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="793e8-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="793e8-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="793e8-118">Header files</span></span>

<span data-ttu-id="793e8-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="793e8-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="793e8-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="793e8-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="793e8-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="793e8-121">Mapitags.h</span></span>
  
> <span data-ttu-id="793e8-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="793e8-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="793e8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="793e8-123">See also</span></span>



[<span data-ttu-id="793e8-124">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="793e8-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="793e8-125">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="793e8-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="793e8-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="793e8-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="793e8-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="793e8-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="793e8-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="793e8-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="793e8-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="793e8-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

