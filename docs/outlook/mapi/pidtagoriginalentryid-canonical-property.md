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
ms.openlocfilehash: d60531b087d00ca63a060a4dbfac559ba3b01788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811452"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="a822a-103">Каноническое свойство PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="a822a-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a822a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a822a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a822a-105">Содержит исходный идентификатор записи для входа, скопированные из адресной книги для Личная адресная книга или других доступным для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a822a-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a822a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a822a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a822a-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a822a-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a822a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a822a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a822a-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="a822a-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="a822a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a822a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a822a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a822a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a822a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a822a-112">Area:</span></span>  <br/> |<span data-ttu-id="a822a-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="a822a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a822a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a822a-114">Remarks</span></span>

<span data-ttu-id="a822a-115">Это свойство является одним из свойств, которые содержат сведения о оригинального источника скопированной запись.</span><span class="sxs-lookup"><span data-stu-id="a822a-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="a822a-116">Для nonread отчета это свойство содержит копию идентификатор записи исходный получатель сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="a822a-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="a822a-117">Если исходный получатель входит в список рассылки, идентификатор записи списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="a822a-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a822a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a822a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a822a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a822a-119">Protocol specifications</span></span>

<span data-ttu-id="a822a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a822a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a822a-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a822a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a822a-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a822a-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a822a-123">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a822a-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="a822a-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a822a-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a822a-125">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="a822a-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a822a-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a822a-126">Header files</span></span>

<span data-ttu-id="a822a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a822a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a822a-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a822a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="a822a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a822a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="a822a-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a822a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a822a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a822a-131">See also</span></span>



[<span data-ttu-id="a822a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a822a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a822a-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a822a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a822a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a822a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a822a-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a822a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

