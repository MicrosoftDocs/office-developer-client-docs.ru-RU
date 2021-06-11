---
title: Каноническое свойство PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358823"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="8e1f4-103">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="8e1f4-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="8e1f4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e1f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e1f4-105">Содержит **PR_ENTRYID** [(PidTagEntryId),](pidtagentryid-canonical-property.md)выраженный как формат постоянного входа.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e1f4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8e1f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e1f4-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="8e1f4-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="8e1f4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8e1f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e1f4-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="8e1f4-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="8e1f4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8e1f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e1f4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8e1f4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8e1f4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8e1f4-112">Area:</span></span>  <br/> |<span data-ttu-id="8e1f4-113">�������� ����� MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1f4-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e1f4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e1f4-114">Remarks</span></span>

<span data-ttu-id="8e1f4-115">Это значение должно присутствовать для всех объектов адресной книги на сервере интерфейса поставщика служб имени (NSPI), его отличительное имя (DN) должно соответствовать значению **PR_EMAIL_ADDRESS** [(PidTagEmailAddress),](pidtagemailaddress-canonical-property.md)а его DN должен следовать спецификации формата DN, определенной типу объекта.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="8e1f4-116">Это свойство не присутствует на объектах в автономной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e1f4-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8e1f4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e1f4-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8e1f4-118">Protocol specifications</span></span>

<span data-ttu-id="8e1f4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e1f4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e1f4-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e1f4-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e1f4-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e1f4-122">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e1f4-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8e1f4-123">Header files</span></span>

<span data-ttu-id="8e1f4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e1f4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e1f4-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e1f4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e1f4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8e1f4-127">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="8e1f4-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e1f4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8e1f4-128">See also</span></span>



[<span data-ttu-id="8e1f4-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1f4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e1f4-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1f4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e1f4-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8e1f4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e1f4-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8e1f4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

