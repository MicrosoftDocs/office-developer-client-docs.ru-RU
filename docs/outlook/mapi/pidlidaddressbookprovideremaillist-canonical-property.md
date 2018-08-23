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
ms.openlocfilehash: 9f73720860aa0ec54289f25a553bb00bfbe76b6a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581050"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="1463f-103">Каноническое свойство PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="1463f-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="1463f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1463f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1463f-105">Указывает, какие свойства электронный адрес, заданные для контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1463f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1463f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1463f-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="1463f-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="1463f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1463f-108">Property set:</span></span>  <br/> |<span data-ttu-id="1463f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1463f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1463f-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1463f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1463f-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="1463f-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="1463f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1463f-112">Data type:</span></span>  <br/> |<span data-ttu-id="1463f-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="1463f-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="1463f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1463f-114">Area:</span></span>  <br/> |<span data-ttu-id="1463f-115">Contact</span><span class="sxs-lookup"><span data-stu-id="1463f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1463f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1463f-116">Remarks</span></span>

<span data-ttu-id="1463f-117">Каждое значение PT_LONG в это свойство должно быть уникальным в свойстве и должна соответствовать одному из значений в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="1463f-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="1463f-118">Если задано это свойство, необходимо также установить свойство **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1463f-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="1463f-119">Эти два свойства должны быть синхронизируется друг с другом.</span><span class="sxs-lookup"><span data-stu-id="1463f-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="1463f-120">Например если выполняется одно из значений в **dispidABPEmailList** «0x00000000», а затем **dispidABPArrayType** необходимо разрядная «0x00000001» установить.</span><span class="sxs-lookup"><span data-stu-id="1463f-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="1463f-121">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1463f-121">**Value**</span></span>|<span data-ttu-id="1463f-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1463f-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1463f-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1463f-123">0x00000000</span></span>  <br/> |<span data-ttu-id="1463f-124">Email1 определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="1463f-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1463f-125">0x00000001</span></span>  <br/> |<span data-ttu-id="1463f-126">Почта2: определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="1463f-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1463f-127">0x00000002</span></span>  <br/> |<span data-ttu-id="1463f-128">Почта3: определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="1463f-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1463f-129">0x00000003</span></span>  <br/> |<span data-ttu-id="1463f-130">Рабочий факс определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="1463f-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1463f-131">0x00000004</span></span>  <br/> |<span data-ttu-id="1463f-132">Домашняя страница факса определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="1463f-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1463f-133">0x00000005</span></span>  <br/> |<span data-ttu-id="1463f-134">Основной факс определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="1463f-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1463f-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1463f-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1463f-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1463f-136">Protocol specifications</span></span>

<span data-ttu-id="1463f-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1463f-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1463f-138">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1463f-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1463f-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1463f-139">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1463f-140">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="1463f-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1463f-141">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1463f-141">Header files</span></span>

<span data-ttu-id="1463f-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1463f-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="1463f-143">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1463f-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1463f-144">См. также</span><span class="sxs-lookup"><span data-stu-id="1463f-144">See also</span></span>



[<span data-ttu-id="1463f-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1463f-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1463f-146">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1463f-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1463f-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1463f-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1463f-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1463f-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

