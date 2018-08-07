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
ms.openlocfilehash: 4a43bc33f13d8325a55d09b5ef3031dc632cf587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811436"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a><span data-ttu-id="13a4a-103">Каноническое свойство PidTagOriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="13a4a-103">PidTagOriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="13a4a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13a4a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13a4a-105">Содержит отображаемое имя записи копируются из адресной книги Личная адресная книга или других для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="13a4a-105">Contains the original display name for an entry copied from an address book to a personal address book or other writable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13a4a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="13a4a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13a4a-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="13a4a-107">PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="13a4a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="13a4a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13a4a-109">0x3A13</span><span class="sxs-lookup"><span data-stu-id="13a4a-109">0x3A13</span></span>  <br/> |
|<span data-ttu-id="13a4a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="13a4a-110">Data type:</span></span>  <br/> |<span data-ttu-id="13a4a-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13a4a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13a4a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="13a4a-112">Area:</span></span>  <br/> |<span data-ttu-id="13a4a-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="13a4a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13a4a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="13a4a-114">Remarks</span></span>

<span data-ttu-id="13a4a-115">Эти свойства содержат сведения о оригинального источника скопированной запись.</span><span class="sxs-lookup"><span data-stu-id="13a4a-115">These properties contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="13a4a-116">Для nonread отчета эти свойства содержит копию отображаемое имя исходный получатель сообщения, для которого создается отчет.</span><span class="sxs-lookup"><span data-stu-id="13a4a-116">For a nonread report, these properties contain a copy of the display name of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="13a4a-117">Если исходный получатель входит в список рассылки, отображаемое имя списка рассылки сохраняется для отчета.</span><span class="sxs-lookup"><span data-stu-id="13a4a-117">When the original recipient is part of a distribution list, the display name of the distribution list is preserved for the report.</span></span>
  
<span data-ttu-id="13a4a-118">Клиентское приложение может использовать эти свойства для предотвращения изменения или «спуфинг» записей, передав неизменными копию отображаемое имя для сравнения.</span><span class="sxs-lookup"><span data-stu-id="13a4a-118">A client application can use these properties to prevent alteration or "spoofing" of entries, by giving an unaltered copy of the display name to compare.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13a4a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13a4a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13a4a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="13a4a-120">Protocol specifications</span></span>

<span data-ttu-id="13a4a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13a4a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13a4a-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13a4a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13a4a-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13a4a-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13a4a-124">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13a4a-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13a4a-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="13a4a-125">Header files</span></span>

<span data-ttu-id="13a4a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13a4a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="13a4a-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="13a4a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="13a4a-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13a4a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="13a4a-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="13a4a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13a4a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="13a4a-130">See also</span></span>



[<span data-ttu-id="13a4a-131">Каноническое свойство PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="13a4a-131">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="13a4a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13a4a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13a4a-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13a4a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13a4a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="13a4a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13a4a-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="13a4a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

