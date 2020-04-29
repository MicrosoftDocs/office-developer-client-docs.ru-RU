---
title: Каноническое свойство PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316158"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="862df-103">Каноническое свойство PidTagGender</span><span class="sxs-lookup"><span data-stu-id="862df-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="862df-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="862df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="862df-105">Содержит Пол пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="862df-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="862df-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="862df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="862df-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="862df-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="862df-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="862df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="862df-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="862df-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="862df-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="862df-110">Data type:</span></span>  <br/> |<span data-ttu-id="862df-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="862df-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="862df-112">Область:</span><span class="sxs-lookup"><span data-stu-id="862df-112">Area:</span></span>  <br/> |<span data-ttu-id="862df-113">Пользователь почты MAPI</span><span class="sxs-lookup"><span data-stu-id="862df-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="862df-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="862df-114">Remarks</span></span>

<span data-ttu-id="862df-115">Это свойство обеспечивает идентификацию и доступ к информации о пользователе обмена сообщениями и его содержимом.</span><span class="sxs-lookup"><span data-stu-id="862df-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="862df-116">Содержимое определяется пользователем обмена сообщениями и организацией пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="862df-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="862df-117">Возможные значения для этого свойства определяются в перечислении Gender.</span><span class="sxs-lookup"><span data-stu-id="862df-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="862df-118">Они перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="862df-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="862df-119">**Перечисление пола**</span><span class="sxs-lookup"><span data-stu-id="862df-119">**Gender enumeration**</span></span>|<span data-ttu-id="862df-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="862df-120">**Value**</span></span>|<span data-ttu-id="862df-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="862df-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="862df-122">жендерунспеЦифиед</span><span class="sxs-lookup"><span data-stu-id="862df-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="862df-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="862df-123">0x0000</span></span>  <br/> |<span data-ttu-id="862df-124">Пол контакта не определен.</span><span class="sxs-lookup"><span data-stu-id="862df-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="862df-125">жендерфемале</span><span class="sxs-lookup"><span data-stu-id="862df-125">genderFemale</span></span>  <br/> |<span data-ttu-id="862df-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="862df-126">0x0001</span></span>  <br/> |<span data-ttu-id="862df-127">Контакт — гнездо.</span><span class="sxs-lookup"><span data-stu-id="862df-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="862df-128">жендермале</span><span class="sxs-lookup"><span data-stu-id="862df-128">genderMale</span></span>  <br/> |<span data-ttu-id="862df-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="862df-129">0x0002</span></span>  <br/> |<span data-ttu-id="862df-130">Контакт имеет значение "штекер".</span><span class="sxs-lookup"><span data-stu-id="862df-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="862df-131">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="862df-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="862df-132">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="862df-132">Protocol specifications</span></span>

<span data-ttu-id="862df-133">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="862df-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="862df-134">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="862df-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="862df-135">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="862df-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="862df-136">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="862df-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="862df-137">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="862df-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="862df-138">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="862df-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="862df-139">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="862df-139">Header files</span></span>

<span data-ttu-id="862df-140">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="862df-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="862df-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="862df-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="862df-142">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="862df-142">Mapitags.h</span></span>
  
> <span data-ttu-id="862df-143">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="862df-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="862df-144">См. также</span><span class="sxs-lookup"><span data-stu-id="862df-144">See also</span></span>



[<span data-ttu-id="862df-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="862df-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="862df-146">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="862df-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="862df-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="862df-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="862df-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="862df-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

