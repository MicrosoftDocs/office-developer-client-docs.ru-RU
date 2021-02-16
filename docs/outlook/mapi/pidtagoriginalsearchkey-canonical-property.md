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
# <a name="pidtagoriginalsearchkey-canonical-property"></a><span data-ttu-id="a94ae-103">Каноническое свойство PidTagOriginalSearchKey</span><span class="sxs-lookup"><span data-stu-id="a94ae-103">PidTagOriginalSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="a94ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a94ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a94ae-105">Содержит исходный ключ поиска для записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="a94ae-105">Contains the original search key for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a94ae-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a94ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a94ae-107">PR_ORIGINAL_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a94ae-107">PR_ORIGINAL_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="a94ae-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a94ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a94ae-109">0x3A14</span><span class="sxs-lookup"><span data-stu-id="a94ae-109">0x3A14</span></span>  <br/> |
|<span data-ttu-id="a94ae-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a94ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="a94ae-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a94ae-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a94ae-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a94ae-112">Area:</span></span>  <br/> |<span data-ttu-id="a94ae-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="a94ae-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a94ae-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a94ae-114">Remarks</span></span>

<span data-ttu-id="a94ae-115">Это свойство является одним из свойств, содержащих сведения об исходном источнике скопированной записи.</span><span class="sxs-lookup"><span data-stu-id="a94ae-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="a94ae-116">В непрочитанном отчете это свойство содержит копию ключа поиска исходного получателя сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="a94ae-116">For a nonread report, this property contains a copy of the search key of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="a94ae-117">Если исходный получатель входит в список рассылки, ключ поиска в списке рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="a94ae-117">When the original recipient is part of a distribution list, the search key of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a94ae-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a94ae-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a94ae-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a94ae-119">Protocol specifications</span></span>

<span data-ttu-id="a94ae-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a94ae-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a94ae-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a94ae-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a94ae-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a94ae-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a94ae-123">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a94ae-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a94ae-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="a94ae-124">Header files</span></span>

<span data-ttu-id="a94ae-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a94ae-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a94ae-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a94ae-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a94ae-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a94ae-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a94ae-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a94ae-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a94ae-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a94ae-129">See also</span></span>



[<span data-ttu-id="a94ae-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a94ae-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a94ae-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a94ae-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a94ae-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a94ae-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a94ae-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a94ae-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

