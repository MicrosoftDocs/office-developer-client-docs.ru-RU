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
ms.openlocfilehash: d106a216e8d72c126f3293f9d492db73992c3872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355295"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="edd17-103">Каноническое свойство PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="edd17-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="edd17-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edd17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edd17-105">Содержит исходный ключ поиска для записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="edd17-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edd17-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="edd17-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edd17-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="edd17-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="edd17-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="edd17-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edd17-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="edd17-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="edd17-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="edd17-110">Data type:</span></span>  <br/> |<span data-ttu-id="edd17-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edd17-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edd17-112">Область:</span><span class="sxs-lookup"><span data-stu-id="edd17-112">Area:</span></span>  <br/> |<span data-ttu-id="edd17-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="edd17-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edd17-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="edd17-114">Remarks</span></span>

<span data-ttu-id="edd17-115">Это свойство является одним из свойств, содержащих сведения о первоначальном источнике скопированной записи.</span><span class="sxs-lookup"><span data-stu-id="edd17-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="edd17-116">Для отчета о непрочтении это свойство содержит копию ключа поиска исходного получателя сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="edd17-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="edd17-117">Когда исходный получатель входит в список рассылки, ключ поиска списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="edd17-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edd17-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="edd17-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edd17-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="edd17-119">Protocol specifications</span></span>

<span data-ttu-id="edd17-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd17-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd17-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="edd17-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edd17-122">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edd17-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edd17-123">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edd17-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edd17-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="edd17-124">Header files</span></span>

<span data-ttu-id="edd17-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="edd17-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="edd17-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="edd17-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="edd17-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="edd17-127">Mapitags.h</span></span>
  
> <span data-ttu-id="edd17-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="edd17-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edd17-129">См. также</span><span class="sxs-lookup"><span data-stu-id="edd17-129">See also</span></span>



[<span data-ttu-id="edd17-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="edd17-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edd17-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="edd17-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edd17-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="edd17-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edd17-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="edd17-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

