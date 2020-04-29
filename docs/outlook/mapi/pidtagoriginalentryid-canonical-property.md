---
title: Каноническое свойство PidTagOriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f3f4f42d91c4091943d6183508e2bc76c17197fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342723"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="6df62-103">Каноническое свойство PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="6df62-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6df62-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6df62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6df62-105">Содержит исходный идентификатор записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="6df62-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6df62-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6df62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6df62-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6df62-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6df62-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6df62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6df62-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="6df62-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="6df62-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6df62-110">Data type:</span></span>  <br/> |<span data-ttu-id="6df62-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6df62-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6df62-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6df62-112">Area:</span></span>  <br/> |<span data-ttu-id="6df62-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="6df62-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6df62-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6df62-114">Remarks</span></span>

<span data-ttu-id="6df62-115">Это свойство является одним из свойств, содержащих сведения о первоначальном источнике скопированной записи.</span><span class="sxs-lookup"><span data-stu-id="6df62-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="6df62-116">Для отчета о непрочтении это свойство содержит копию идентификатора записи исходного получателя сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="6df62-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="6df62-117">Когда исходный получатель входит в список рассылки, идентификатор записи списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="6df62-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6df62-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6df62-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6df62-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6df62-119">Protocol specifications</span></span>

<span data-ttu-id="6df62-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6df62-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6df62-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6df62-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6df62-122">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6df62-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6df62-123">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6df62-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6df62-124">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6df62-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6df62-125">Обрабатывает синхронизацию данных объекта обмена данными между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="6df62-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6df62-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6df62-126">Header files</span></span>

<span data-ttu-id="6df62-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6df62-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6df62-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6df62-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6df62-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6df62-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6df62-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="6df62-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6df62-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6df62-131">See also</span></span>



[<span data-ttu-id="6df62-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6df62-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6df62-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6df62-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6df62-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6df62-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6df62-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6df62-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

