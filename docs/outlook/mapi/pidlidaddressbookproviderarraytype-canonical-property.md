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
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810086"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a><span data-ttu-id="c49c3-103">Каноническое свойство PidLidAddressBookProviderArrayType</span><span class="sxs-lookup"><span data-stu-id="c49c3-103">PidLidAddressBookProviderArrayType Canonical Property</span></span>

  
  
<span data-ttu-id="c49c3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c49c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c49c3-105">Указывает состояние контакта электронных адресов и представляет набор битовых флагов.</span><span class="sxs-lookup"><span data-stu-id="c49c3-105">Specifies the state of the contact's electronic addresses and represents a set of bit flags.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c49c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c49c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c49c3-107">dispidABPArrayType</span><span class="sxs-lookup"><span data-stu-id="c49c3-107">dispidABPArrayType</span></span>  <br/> |
|<span data-ttu-id="c49c3-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c49c3-108">Property set:</span></span>  <br/> |<span data-ttu-id="c49c3-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c49c3-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c49c3-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c49c3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c49c3-111">0x00008029</span><span class="sxs-lookup"><span data-stu-id="c49c3-111">0x00008029</span></span>  <br/> |
|<span data-ttu-id="c49c3-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c49c3-112">Data type:</span></span>  <br/> |<span data-ttu-id="c49c3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c49c3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c49c3-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c49c3-114">Area:</span></span>  <br/> |<span data-ttu-id="c49c3-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="c49c3-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c49c3-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c49c3-116">Remarks</span></span>

<span data-ttu-id="c49c3-117">Значение свойства **dispidABPArrayType** должно быть сочетание флаги, определяющие состояние объекта контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-117">The value of the **dispidABPArrayType** property must be a combination of flags that specify the state of the contact object.</span></span> <span data-ttu-id="c49c3-118">В следующей таблице указаны отдельные флаги.</span><span class="sxs-lookup"><span data-stu-id="c49c3-118">Individual flags are specified in the following table.</span></span> <span data-ttu-id="c49c3-119">Если задано это свойство, свойство **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) необходимо установить, а также.</span><span class="sxs-lookup"><span data-stu-id="c49c3-119">If this property is set, the **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) property must be set, as well.</span></span> <span data-ttu-id="c49c3-120">Эти два свойства должны быть синхронизируется друг с другом.</span><span class="sxs-lookup"><span data-stu-id="c49c3-120">These two properties must be kept synchronized with each other.</span></span> <span data-ttu-id="c49c3-121">К примеру Если **dispidABPArrayType** разрядная «0x00000001 set», одно из значений **dispidABPEmailList** значения «0x00000000».</span><span class="sxs-lookup"><span data-stu-id="c49c3-121">For example, if **dispidABPArrayType** has the bit "0x00000001 set", one of the values of **dispidABPEmailList** must be "0x00000000".</span></span> 
  
|<span data-ttu-id="c49c3-122">**Бит**</span><span class="sxs-lookup"><span data-stu-id="c49c3-122">**Bit**</span></span>|<span data-ttu-id="c49c3-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c49c3-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c49c3-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c49c3-124">0x00000001</span></span>  <br/> |<span data-ttu-id="c49c3-125">Email1 определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-125">Email1 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c49c3-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c49c3-126">0x00000002</span></span>  <br/> |<span data-ttu-id="c49c3-127">Почта2: определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-127">Email2 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c49c3-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c49c3-128">0x00000004</span></span>  <br/> |<span data-ttu-id="c49c3-129">Почта3: определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-129">Email3 is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c49c3-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c49c3-130">0x00000008</span></span>  <br/> |<span data-ttu-id="c49c3-131">Рабочий факс определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-131">Business fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c49c3-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c49c3-132">0x00000010</span></span>  <br/> |<span data-ttu-id="c49c3-133">Домашняя страница факса определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-133">Home fax is defined for the contact.</span></span>  <br/> |
|<span data-ttu-id="c49c3-134">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c49c3-134">0x00000020</span></span>  <br/> |<span data-ttu-id="c49c3-135">Основной факс определяется для этого контакта.</span><span class="sxs-lookup"><span data-stu-id="c49c3-135">Primary fax is defined for the contact.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c49c3-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c49c3-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c49c3-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c49c3-137">Protocol specifications</span></span>

<span data-ttu-id="c49c3-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c49c3-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c49c3-139">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c49c3-139">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c49c3-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c49c3-140">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c49c3-141">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="c49c3-141">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c49c3-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c49c3-142">Header files</span></span>

<span data-ttu-id="c49c3-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c49c3-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="c49c3-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c49c3-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c49c3-145">См. также</span><span class="sxs-lookup"><span data-stu-id="c49c3-145">See also</span></span>



[<span data-ttu-id="c49c3-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c49c3-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c49c3-147">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c49c3-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c49c3-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c49c3-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c49c3-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c49c3-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

