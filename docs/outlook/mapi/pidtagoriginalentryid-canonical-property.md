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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391045"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="7d2c2-103">Каноническое свойство PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="7d2c2-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7d2c2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d2c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d2c2-105">Содержит исходный идентификатор записи для входа, скопированные из адресной книги для Личная адресная книга или других доступным для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d2c2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7d2c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d2c2-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7d2c2-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7d2c2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7d2c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d2c2-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="7d2c2-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="7d2c2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7d2c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d2c2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d2c2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7d2c2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7d2c2-112">Area:</span></span>  <br/> |<span data-ttu-id="7d2c2-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="7d2c2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d2c2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7d2c2-114">Remarks</span></span>

<span data-ttu-id="7d2c2-115">Это свойство является одним из свойств, которые содержат сведения о оригинального источника скопированной запись.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="7d2c2-116">Для nonread отчета это свойство содержит копию идентификатор записи исходный получатель сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="7d2c2-117">Если исходный получатель входит в список рассылки, идентификатор записи списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d2c2-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7d2c2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d2c2-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7d2c2-119">Protocol specifications</span></span>

<span data-ttu-id="7d2c2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d2c2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d2c2-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d2c2-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d2c2-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d2c2-123">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="7d2c2-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d2c2-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d2c2-125">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d2c2-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7d2c2-126">Header files</span></span>

<span data-ttu-id="7d2c2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d2c2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d2c2-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d2c2-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d2c2-129">Mapitags.h</span></span>
  
> <span data-ttu-id="7d2c2-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7d2c2-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d2c2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7d2c2-131">See also</span></span>



[<span data-ttu-id="7d2c2-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d2c2-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d2c2-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7d2c2-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d2c2-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7d2c2-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

