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
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a><span data-ttu-id="0f789-103">Каноническое свойство PidLidAddressBookProviderEmailList</span><span class="sxs-lookup"><span data-stu-id="0f789-103">PidLidAddressBookProviderEmailList Canonical Property</span></span>

  
  
<span data-ttu-id="0f789-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f789-105">Указывает, какие свойства электронных адресов заданы для контакта.</span><span class="sxs-lookup"><span data-stu-id="0f789-105">Specifies which electronic address properties are set on the contact.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f789-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0f789-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f789-107">dispidABPEmailList</span><span class="sxs-lookup"><span data-stu-id="0f789-107">dispidABPEmailList</span></span>  <br/> |
|<span data-ttu-id="0f789-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0f789-108">Property set:</span></span>  <br/> |<span data-ttu-id="0f789-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="0f789-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0f789-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0f789-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0f789-111">0x00008028</span><span class="sxs-lookup"><span data-stu-id="0f789-111">0x00008028</span></span>  <br/> |
|<span data-ttu-id="0f789-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f789-112">Data type:</span></span>  <br/> |<span data-ttu-id="0f789-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="0f789-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="0f789-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0f789-114">Area:</span></span>  <br/> |<span data-ttu-id="0f789-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="0f789-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f789-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f789-116">Remarks</span></span>

<span data-ttu-id="0f789-117">Каждое PT_LONG этого свойства должно быть уникальным в свойстве и должно иметь одно из значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0f789-117">Each PT_LONG value in this property must be unique in the property and must be set to one of the values in the following table.</span></span> <span data-ttu-id="0f789-118">Если за установлено это свойство, необходимо также установить свойство **dispidABPArrayType** ([PidLidAddressBookProviderArrayType).](pidlidaddressbookproviderarraytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0f789-118">If this property is set, the **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="0f789-119">Эти два свойства должны синхронизироваться друг с другом.</span><span class="sxs-lookup"><span data-stu-id="0f789-119">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="0f789-120">Например, если одно из значений **в dispidABPEmailList** — "0x00000000", то **dispidABPArrayType** должен иметь бит "0x00000001".</span><span class="sxs-lookup"><span data-stu-id="0f789-120">For example, if one of the values in **dispidABPEmailList** is "0x00000000", then **dispidABPArrayType** must have the bit "0x00000001" set.</span></span> 
  
|<span data-ttu-id="0f789-121">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0f789-121">**Value**</span></span>|<span data-ttu-id="0f789-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f789-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f789-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0f789-123">0x00000000</span></span>  <br/> |<span data-ttu-id="0f789-124">Для контакта определена электронная почта 1.</span><span class="sxs-lookup"><span data-stu-id="0f789-124">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0f789-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0f789-125">0x00000001</span></span>  <br/> |<span data-ttu-id="0f789-126">Для контакта определена электронная почта 2.</span><span class="sxs-lookup"><span data-stu-id="0f789-126">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0f789-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0f789-127">0x00000002</span></span>  <br/> |<span data-ttu-id="0f789-128">Для контакта определена электронная почта 3.</span><span class="sxs-lookup"><span data-stu-id="0f789-128">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0f789-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="0f789-129">0x00000003</span></span>  <br/> |<span data-ttu-id="0f789-130">Для контакта определена деловая факсимиловая связь.</span><span class="sxs-lookup"><span data-stu-id="0f789-130">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0f789-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0f789-131">0x00000004</span></span>  <br/> |<span data-ttu-id="0f789-132">Для контакта определена домашняя факсимиловая связь.</span><span class="sxs-lookup"><span data-stu-id="0f789-132">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0f789-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0f789-133">0x00000005</span></span>  <br/> |<span data-ttu-id="0f789-134">Основной факс определяется для контакта.</span><span class="sxs-lookup"><span data-stu-id="0f789-134">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0f789-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0f789-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f789-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0f789-136">Protocol specifications</span></span>

<span data-ttu-id="0f789-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f789-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f789-138">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="0f789-138">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f789-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f789-139">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f789-140">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="0f789-140">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f789-141">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="0f789-141">Header files</span></span>

<span data-ttu-id="0f789-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f789-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f789-143">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0f789-143">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f789-144">См. также</span><span class="sxs-lookup"><span data-stu-id="0f789-144">See also</span></span>



[<span data-ttu-id="0f789-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0f789-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f789-146">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0f789-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f789-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0f789-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f789-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0f789-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

