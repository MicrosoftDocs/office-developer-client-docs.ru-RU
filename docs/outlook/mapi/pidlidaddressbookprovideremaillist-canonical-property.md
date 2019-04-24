---
title: Каноническое свойство PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348484"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="ce600-103">Каноническое свойство PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="ce600-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="ce600-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce600-105">Указывает, какие свойства электронных адресов для контакта задаются.</span><span class="sxs-lookup"><span data-stu-id="ce600-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce600-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ce600-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce600-107">Диспидабпемаиллист</span><span class="sxs-lookup"><span data-stu-id="ce600-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="ce600-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ce600-108">Property set:</span></span>  <br/> |<span data-ttu-id="ce600-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="ce600-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ce600-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="ce600-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ce600-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="ce600-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="ce600-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ce600-112">Data type:</span></span>  <br/> |<span data-ttu-id="ce600-113">ПТ_МВ_ЛОНГ</span><span class="sxs-lookup"><span data-stu-id="ce600-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ce600-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ce600-114">Area:</span></span>  <br/> |<span data-ttu-id="ce600-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="ce600-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce600-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce600-116">Remarks</span></span>

<span data-ttu-id="ce600-117">Каждое значение ПТ_ЛОНГ в этом свойстве должно быть уникальным в свойстве и должно быть равно одному из значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ce600-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="ce600-118">Если это свойство задано, также должно быть задано свойство **диспидабпаррайтипе** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce600-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="ce600-119">Эти два свойства должны поддерживать синхронизацию друг с другом.</span><span class="sxs-lookup"><span data-stu-id="ce600-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="ce600-120">Например, если одно из значений в **диспидабпемаиллист** имеет значение "0x00000000", то **диспидабпаррайтипе** должен иметь бит "0x00000001".</span><span class="sxs-lookup"><span data-stu-id="ce600-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="ce600-121">**Value**</span><span class="sxs-lookup"><span data-stu-id="ce600-121">**Value**</span></span>|<span data-ttu-id="ce600-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce600-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce600-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce600-123">0x00000000</span></span>  <br/> |<span data-ttu-id="ce600-124">Для контакта определено значение Email1.</span><span class="sxs-lookup"><span data-stu-id="ce600-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ce600-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce600-125">0x00000001</span></span>  <br/> |<span data-ttu-id="ce600-126">Для контакта определено значение Email2.</span><span class="sxs-lookup"><span data-stu-id="ce600-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ce600-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ce600-127">0x00000002</span></span>  <br/> |<span data-ttu-id="ce600-128">Для контакта определено значение Email3.</span><span class="sxs-lookup"><span data-stu-id="ce600-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ce600-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ce600-129">0x00000003</span></span>  <br/> |<span data-ttu-id="ce600-130">Для контакта определен рабочий Факс.</span><span class="sxs-lookup"><span data-stu-id="ce600-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ce600-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ce600-131">0x00000004</span></span>  <br/> |<span data-ttu-id="ce600-132">Для контакта определен домашний Факс.</span><span class="sxs-lookup"><span data-stu-id="ce600-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="ce600-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ce600-133">0x00000005</span></span>  <br/> |<span data-ttu-id="ce600-134">Для контакта определен основной Факс.</span><span class="sxs-lookup"><span data-stu-id="ce600-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ce600-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ce600-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ce600-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ce600-136">Protocol specifications</span></span>

<span data-ttu-id="ce600-137">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce600-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce600-138">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ce600-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ce600-139">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce600-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce600-140">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="ce600-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ce600-141">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ce600-141">Header files</span></span>

<span data-ttu-id="ce600-142">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ce600-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce600-143">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ce600-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce600-144">См. также</span><span class="sxs-lookup"><span data-stu-id="ce600-144">See also</span></span>



[<span data-ttu-id="ce600-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce600-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce600-146">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ce600-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce600-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ce600-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce600-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ce600-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

