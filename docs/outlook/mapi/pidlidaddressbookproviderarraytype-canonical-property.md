---
title: Каноническое свойство PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348442"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="f50d3-103">Каноническое свойство PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="f50d3-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="f50d3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f50d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f50d3-105">Указывает состояние электронных адресов контакта и представляет набор битных флагов.</span><span class="sxs-lookup"><span data-stu-id="f50d3-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f50d3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f50d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f50d3-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="f50d3-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="f50d3-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f50d3-108">Property set:</span></span>  <br/> |<span data-ttu-id="f50d3-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="f50d3-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="f50d3-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f50d3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f50d3-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="f50d3-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="f50d3-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f50d3-112">Data type:</span></span>  <br/> |<span data-ttu-id="f50d3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f50d3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f50d3-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f50d3-114">Area:</span></span>  <br/> |<span data-ttu-id="f50d3-115">Contact</span><span class="sxs-lookup"><span data-stu-id="f50d3-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f50d3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f50d3-116">Remarks</span></span>

<span data-ttu-id="f50d3-117">Значение свойства **dispidABPArrayType** должно быть сочетанием флагов, которые указывают состояние контактного объекта.</span><span class="sxs-lookup"><span data-stu-id="f50d3-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="f50d3-118">Отдельные флаги указаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f50d3-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="f50d3-119">Если это свойство заданной, необходимо также задать свойство **dispidABPEmailList** [(PidLidAddressBookProviderEmailList).](pidlidaddressbookprovideremaillist-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f50d3-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="f50d3-120">Эти два свойства должны синхронизироваться друг с другом.</span><span class="sxs-lookup"><span data-stu-id="f50d3-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="f50d3-121">Например, если **dispidABPArrayType** имеет бит "0x00000001 набор", одно из значений **dispidABPEmailList** должно быть "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="f50d3-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="f50d3-122">**Bit**</span><span class="sxs-lookup"><span data-stu-id="f50d3-122">**Bit**</span></span>|<span data-ttu-id="f50d3-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f50d3-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f50d3-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f50d3-124">0x00000001</span></span>  <br/> |<span data-ttu-id="f50d3-125">Email1 определяется для контакта.</span><span class="sxs-lookup"><span data-stu-id="f50d3-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="f50d3-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f50d3-126">0x00000002</span></span>  <br/> |<span data-ttu-id="f50d3-127">Email2 определяется для контакта.</span><span class="sxs-lookup"><span data-stu-id="f50d3-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="f50d3-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f50d3-128">0x00000004</span></span>  <br/> |<span data-ttu-id="f50d3-129">Email3 определяется для контакта.</span><span class="sxs-lookup"><span data-stu-id="f50d3-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="f50d3-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f50d3-130">0x00000008</span></span>  <br/> |<span data-ttu-id="f50d3-131">Для контакта определяется бизнес-факс.</span><span class="sxs-lookup"><span data-stu-id="f50d3-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="f50d3-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f50d3-132">0x00000010</span></span>  <br/> |<span data-ttu-id="f50d3-133">Для контакта определяется домашний факс.</span><span class="sxs-lookup"><span data-stu-id="f50d3-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="f50d3-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f50d3-134">0x00000020</span></span>  <br/> |<span data-ttu-id="f50d3-135">Для контакта определяется первичный факс.</span><span class="sxs-lookup"><span data-stu-id="f50d3-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f50d3-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f50d3-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f50d3-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f50d3-137">Protocol specifications</span></span>

<span data-ttu-id="f50d3-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f50d3-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f50d3-139">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f50d3-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f50d3-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f50d3-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f50d3-141">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="f50d3-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f50d3-142">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f50d3-142">Header files</span></span>

<span data-ttu-id="f50d3-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f50d3-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="f50d3-144">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f50d3-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f50d3-145">См. также</span><span class="sxs-lookup"><span data-stu-id="f50d3-145">See also</span></span>



[<span data-ttu-id="f50d3-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f50d3-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f50d3-147">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f50d3-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f50d3-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f50d3-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f50d3-149">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f50d3-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

