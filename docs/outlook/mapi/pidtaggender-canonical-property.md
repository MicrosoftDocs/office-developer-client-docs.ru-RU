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
ms.openlocfilehash: b2ac7aa4fca8583fc59d727c55433108bee62dee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811185"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="464ae-103">Каноническое свойство PidTagGender</span><span class="sxs-lookup"><span data-stu-id="464ae-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="464ae-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="464ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="464ae-105">Содержит Пол обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="464ae-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="464ae-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="464ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="464ae-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="464ae-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="464ae-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="464ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="464ae-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="464ae-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="464ae-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="464ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="464ae-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="464ae-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="464ae-112">Область:</span><span class="sxs-lookup"><span data-stu-id="464ae-112">Area:</span></span>  <br/> |<span data-ttu-id="464ae-113">Пользователь почты MAPI</span><span class="sxs-lookup"><span data-stu-id="464ae-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="464ae-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="464ae-114">Remarks</span></span>

<span data-ttu-id="464ae-115">Это свойство обеспечивает идентификации и доступа к сведениям о обмена сообщениями пользователя и контент.</span><span class="sxs-lookup"><span data-stu-id="464ae-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="464ae-116">Содержимое определяется с сообщениями пользователей и организаций обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="464ae-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="464ae-117">Возможные значения для этого свойства определены в перечислении пол.</span><span class="sxs-lookup"><span data-stu-id="464ae-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="464ae-118">Они перечислены в списке следующим образом:</span><span class="sxs-lookup"><span data-stu-id="464ae-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="464ae-119">**Перечисление пол**</span><span class="sxs-lookup"><span data-stu-id="464ae-119">**Gender enumeration**</span></span>|<span data-ttu-id="464ae-120">**Значение**</span><span class="sxs-lookup"><span data-stu-id="464ae-120">**Value**</span></span>|<span data-ttu-id="464ae-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="464ae-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="464ae-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="464ae-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="464ae-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="464ae-123">0x0000</span></span>  <br/> |<span data-ttu-id="464ae-124">Пол контакта не определено.</span><span class="sxs-lookup"><span data-stu-id="464ae-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="464ae-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="464ae-125">genderFemale</span></span>  <br/> |<span data-ttu-id="464ae-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="464ae-126">0x0001</span></span>  <br/> |<span data-ttu-id="464ae-127">Контакт гнездо.</span><span class="sxs-lookup"><span data-stu-id="464ae-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="464ae-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="464ae-128">genderMale</span></span>  <br/> |<span data-ttu-id="464ae-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="464ae-129">0x0002</span></span>  <br/> |<span data-ttu-id="464ae-130">Контакт штекер.</span><span class="sxs-lookup"><span data-stu-id="464ae-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="464ae-131">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="464ae-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="464ae-132">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="464ae-132">Protocol specifications</span></span>

<span data-ttu-id="464ae-133">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="464ae-133">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="464ae-134">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="464ae-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="464ae-135">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="464ae-135">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="464ae-136">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="464ae-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="464ae-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="464ae-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="464ae-138">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="464ae-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="464ae-139">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="464ae-139">Header files</span></span>

<span data-ttu-id="464ae-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="464ae-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="464ae-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="464ae-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="464ae-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="464ae-142">Mapitags.h</span></span>
  
> <span data-ttu-id="464ae-143">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="464ae-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="464ae-144">См. также</span><span class="sxs-lookup"><span data-stu-id="464ae-144">See also</span></span>



[<span data-ttu-id="464ae-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="464ae-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="464ae-146">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="464ae-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="464ae-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="464ae-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="464ae-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="464ae-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

