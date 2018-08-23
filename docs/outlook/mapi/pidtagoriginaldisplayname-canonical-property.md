---
title: Каноническое свойство PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d168082a16ad5e8df205d976349fd6406d9d18a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570774"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="81104-103">Каноническое свойство PidTagOriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="81104-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="81104-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81104-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81104-105">Содержит отображаемое имя записи копируются из адресной книги Личная адресная книга или других для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="81104-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81104-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="81104-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81104-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="81104-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="81104-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="81104-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81104-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="81104-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="81104-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="81104-110">Data type:</span></span>  <br/> |<span data-ttu-id="81104-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="81104-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="81104-112">Область:</span><span class="sxs-lookup"><span data-stu-id="81104-112">Area:</span></span>  <br/> |<span data-ttu-id="81104-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="81104-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81104-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="81104-114">Remarks</span></span>

<span data-ttu-id="81104-115">Эти свойства содержат сведения о оригинального источника скопированной запись.</span><span class="sxs-lookup"><span data-stu-id="81104-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="81104-116">Для nonread отчета эти свойства содержит копию отображаемое имя исходный получатель сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="81104-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="81104-117">Если исходный получатель входит в список рассылки, отображаемое имя списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="81104-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="81104-118">Клиентское приложение может использовать эти свойства для предотвращения изменения или «спуфинг» записей, передав неизменными копию отображаемое имя для сравнения.</span><span class="sxs-lookup"><span data-stu-id="81104-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="81104-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="81104-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81104-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="81104-120">Protocol specifications</span></span>

<span data-ttu-id="81104-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81104-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81104-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="81104-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81104-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81104-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81104-124">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81104-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81104-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="81104-125">Header files</span></span>

<span data-ttu-id="81104-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81104-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="81104-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="81104-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="81104-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81104-128">Mapitags.h</span></span>
  
> <span data-ttu-id="81104-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="81104-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81104-130">См. также</span><span class="sxs-lookup"><span data-stu-id="81104-130">See also</span></span>



[<span data-ttu-id="81104-131">Каноническое свойство PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="81104-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="81104-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="81104-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81104-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="81104-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81104-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="81104-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81104-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="81104-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

