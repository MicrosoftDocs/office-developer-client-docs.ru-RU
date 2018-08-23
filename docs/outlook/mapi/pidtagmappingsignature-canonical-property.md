---
title: Каноническое свойство PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6017871b9567406af0898eede0d5659b468b3343
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581036"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="8558a-103">Каноническое свойство PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="8558a-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="8558a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8558a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8558a-105">Содержит сопоставления подпись для именованных свойств конкретного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="8558a-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8558a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8558a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8558a-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="8558a-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="8558a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8558a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8558a-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="8558a-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="8558a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8558a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8558a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8558a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8558a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8558a-112">Area:</span></span>  <br/> |<span data-ttu-id="8558a-113">Разное</span><span class="sxs-lookup"><span data-stu-id="8558a-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8558a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8558a-114">Remarks</span></span>

<span data-ttu-id="8558a-115">Рекомендуется, что объекты, с именем свойства предоставляют это свойство.</span><span class="sxs-lookup"><span data-stu-id="8558a-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="8558a-116">Клиентское приложение должно проверять свойство **PR_MAPPING_SIGNATURE** обоих объектов при копировании с именем свойства из одного объекта в другой.</span><span class="sxs-lookup"><span data-stu-id="8558a-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="8558a-117">Использование этого свойства можно свести к минимуму преобразование между имена и идентификаторы скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="8558a-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="8558a-118">Если это свойство не существует для того или иного объекта MAPI, объект имеет свой собственный уникальное сопоставление имен и идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="8558a-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="8558a-119">В этом случае клиента необходимо вызвать метод [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) на объекте источника и затем [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="8558a-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="8558a-120">Если два объекта имеют такое же значение **PR_MAPPING_SIGNATURE** , клиент переводить имя, идентификатор и идентификатор имени не требуется.</span><span class="sxs-lookup"><span data-stu-id="8558a-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="8558a-121">Клиент может просто вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) для источника, и затем метод [IMAPIProp::SetProps](imapiprop-setprops.md) в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="8558a-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="8558a-122">Это удобно для клиентов, выполняющие настраиваемые копирование именованных свойств, а также для реализации методов [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMAPIProp::CopyProps](imapiprop-copyprops.md) поставщиков.</span><span class="sxs-lookup"><span data-stu-id="8558a-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="8558a-123">Дополнительные сведения об именованных свойств и сопоставлений имен и идентификаторов в разделе [Свойства с именем MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8558a-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8558a-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8558a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8558a-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8558a-125">Protocol specifications</span></span>

<span data-ttu-id="8558a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8558a-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8558a-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8558a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8558a-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8558a-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8558a-129">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8558a-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8558a-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8558a-130">Header files</span></span>

<span data-ttu-id="8558a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8558a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="8558a-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8558a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="8558a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8558a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="8558a-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8558a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8558a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="8558a-135">See also</span></span>



[<span data-ttu-id="8558a-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="8558a-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="8558a-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8558a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8558a-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8558a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8558a-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8558a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8558a-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8558a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

