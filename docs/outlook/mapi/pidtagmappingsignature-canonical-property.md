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
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342550"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="d526c-103">Каноническое свойство PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="d526c-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="d526c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d526c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d526c-105">Содержит подпись сопоставления для именованных свойств определенного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="d526c-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d526c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d526c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d526c-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="d526c-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="d526c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d526c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d526c-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="d526c-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="d526c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d526c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d526c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d526c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d526c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d526c-112">Area:</span></span>  <br/> |<span data-ttu-id="d526c-113">Разное</span><span class="sxs-lookup"><span data-stu-id="d526c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d526c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d526c-114">Remarks</span></span>

<span data-ttu-id="d526c-115">Для объектов с именованными свойствами рекомендуется предоставлять это свойство.</span><span class="sxs-lookup"><span data-stu-id="d526c-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="d526c-116">Клиентское приложение должно проверять свойство **PR_MAPPING_SIGNATURE** обоих объектов при копировании именованных свойств из одного объекта в другой.</span><span class="sxs-lookup"><span data-stu-id="d526c-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="d526c-117">С помощью этого свойства можно свести к минимуму преобразование между скопированными свойствами и именами и идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="d526c-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="d526c-118">Если это свойство не существует для данного объекта MAPI, объект имеет собственное уникальное сопоставление имен и идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="d526c-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="d526c-119">В этом случае клиент должен вызвать метод [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) для исходного объекта, а затем метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d526c-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="d526c-120">Если два объекта имеют одно и то же значение **PR_MAPPING_SIGNATURE** , клиенту не требуется переводить имя в идентификатор и идентификатор в имя.</span><span class="sxs-lookup"><span data-stu-id="d526c-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="d526c-121">Клиент может просто вызвать метод [IMAPIProp::/PROPS](imapiprop-getprops.md) для источника, а затем метод [IMAPIProp:: SetProps](imapiprop-setprops.md) для назначения.</span><span class="sxs-lookup"><span data-stu-id="d526c-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="d526c-122">Это удобно для клиентов, которые выполняют пользовательское копирование именованных свойств и поставщиков, реализующих методы [IMAPIProp:: CopyTo](imapiprop-copyto.md) и [IMAPIProp:: копипропс](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d526c-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="d526c-123">Дополнительные сведения об именованных свойствах и сопоставлении имен и идентификаторов приведены в статье [свойства MAPI с именем](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d526c-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d526c-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d526c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d526c-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d526c-125">Protocol specifications</span></span>

<span data-ttu-id="d526c-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d526c-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d526c-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d526c-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d526c-128">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d526c-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d526c-129">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d526c-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d526c-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d526c-130">Header files</span></span>

<span data-ttu-id="d526c-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d526c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="d526c-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d526c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="d526c-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d526c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="d526c-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d526c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d526c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d526c-135">See also</span></span>



[<span data-ttu-id="d526c-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="d526c-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="d526c-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d526c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d526c-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d526c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d526c-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d526c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d526c-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d526c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

