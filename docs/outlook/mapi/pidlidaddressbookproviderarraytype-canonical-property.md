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
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="0a386-103">Каноническое свойство PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="0a386-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="0a386-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a386-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a386-105">Указывает состояние электронных адресов контакта и представляет набор битовых флагов.</span><span class="sxs-lookup"><span data-stu-id="0a386-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a386-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0a386-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a386-107">Диспидабпаррайтипе</span><span class="sxs-lookup"><span data-stu-id="0a386-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="0a386-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0a386-108">Property set:</span></span>  <br/> |<span data-ttu-id="0a386-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="0a386-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0a386-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="0a386-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0a386-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="0a386-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="0a386-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0a386-112">Data type:</span></span>  <br/> |<span data-ttu-id="0a386-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0a386-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0a386-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0a386-114">Area:</span></span>  <br/> |<span data-ttu-id="0a386-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="0a386-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a386-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a386-116">Remarks</span></span>

<span data-ttu-id="0a386-117">Значение свойства **диспидабпаррайтипе** должно быть сочетанием флагов, определяющих состояние объекта Contact.</span><span class="sxs-lookup"><span data-stu-id="0a386-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="0a386-118">Отдельные флаги указаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0a386-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="0a386-119">Если это свойство задано, необходимо также задать свойство **диспидабпемаиллист** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0a386-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="0a386-120">Эти два свойства должны поддерживать синхронизацию друг с другом.</span><span class="sxs-lookup"><span data-stu-id="0a386-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="0a386-121">Например, если **диспидабпаррайтипе** имеет бит "0x00000001 набор", то одно из значений **диспидабпемаиллист** должно быть "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="0a386-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="0a386-122">**Битовая**</span><span class="sxs-lookup"><span data-stu-id="0a386-122">**Bit**</span></span>|<span data-ttu-id="0a386-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a386-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a386-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0a386-124">0x00000001</span></span>  <br/> |<span data-ttu-id="0a386-125">Для контакта определено значение Email1.</span><span class="sxs-lookup"><span data-stu-id="0a386-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0a386-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0a386-126">0x00000002</span></span>  <br/> |<span data-ttu-id="0a386-127">Для контакта определено значение Email2.</span><span class="sxs-lookup"><span data-stu-id="0a386-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0a386-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="0a386-128">0x00000004</span></span>  <br/> |<span data-ttu-id="0a386-129">Для контакта определено значение Email3.</span><span class="sxs-lookup"><span data-stu-id="0a386-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0a386-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0a386-130">0x00000008</span></span>  <br/> |<span data-ttu-id="0a386-131">Для контакта определен рабочий Факс.</span><span class="sxs-lookup"><span data-stu-id="0a386-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0a386-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0a386-132">0x00000010</span></span>  <br/> |<span data-ttu-id="0a386-133">Для контакта определен домашний Факс.</span><span class="sxs-lookup"><span data-stu-id="0a386-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="0a386-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="0a386-134">0x00000020</span></span>  <br/> |<span data-ttu-id="0a386-135">Для контакта определен основной Факс.</span><span class="sxs-lookup"><span data-stu-id="0a386-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0a386-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a386-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a386-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0a386-137">Protocol specifications</span></span>

<span data-ttu-id="0a386-138">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a386-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a386-139">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0a386-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a386-140">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a386-140">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a386-141">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="0a386-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a386-142">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="0a386-142">Header files</span></span>

<span data-ttu-id="0a386-143">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0a386-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a386-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0a386-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a386-145">См. также</span><span class="sxs-lookup"><span data-stu-id="0a386-145">See also</span></span>



[<span data-ttu-id="0a386-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a386-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a386-147">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0a386-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a386-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0a386-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a386-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0a386-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

