---
title: Каноническое свойство PidTagOriginalSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26854b640669bbc6479ce90ba9cad18cdf4d9264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811474"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="4ef84-103">Каноническое свойство PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="4ef84-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="4ef84-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ef84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ef84-105">Содержит исходного ключа поиска для записи, скопированные из адресной книги для Личная адресная книга или других доступным для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4ef84-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ef84-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4ef84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ef84-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="4ef84-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="4ef84-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4ef84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ef84-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="4ef84-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="4ef84-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4ef84-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ef84-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ef84-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ef84-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4ef84-112">Area:</span></span>  <br/> |<span data-ttu-id="4ef84-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="4ef84-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ef84-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ef84-114">Remarks</span></span>

<span data-ttu-id="4ef84-115">Это свойство является одним из свойств, которые содержат сведения о оригинального источника скопированной запись.</span><span class="sxs-lookup"><span data-stu-id="4ef84-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="4ef84-116">Для nonread отчета это свойство содержит копию ключ поиска исходный получатель сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="4ef84-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="4ef84-117">Если исходный получатель входит в список рассылки, ключ поиска списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="4ef84-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ef84-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4ef84-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ef84-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4ef84-119">Protocol specifications</span></span>

<span data-ttu-id="4ef84-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ef84-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ef84-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4ef84-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ef84-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ef84-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ef84-123">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ef84-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ef84-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4ef84-124">Header files</span></span>

<span data-ttu-id="4ef84-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ef84-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ef84-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4ef84-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ef84-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ef84-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4ef84-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4ef84-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ef84-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4ef84-129">See also</span></span>



[<span data-ttu-id="4ef84-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef84-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ef84-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef84-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ef84-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef84-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ef84-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4ef84-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

