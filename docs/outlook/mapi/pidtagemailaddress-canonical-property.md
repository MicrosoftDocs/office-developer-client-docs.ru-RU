---
title: Каноническое свойство PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338642"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="aebd5-103">Каноническое свойство PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="aebd5-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="aebd5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aebd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aebd5-105">Содержит адрес электронной почты пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="aebd5-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aebd5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="aebd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aebd5-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="aebd5-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="aebd5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="aebd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aebd5-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="aebd5-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="aebd5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="aebd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="aebd5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aebd5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aebd5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="aebd5-112">Area:</span></span>  <br/> |<span data-ttu-id="aebd5-113">MAPI общие</span><span class="sxs-lookup"><span data-stu-id="aebd5-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aebd5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="aebd5-114">Remarks</span></span>

<span data-ttu-id="aebd5-115">Эти свойства являются примерами свойств базовых адресов для всех пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="aebd5-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="aebd5-116">Это строка с null-terminated, формат которой имеет значение только для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="aebd5-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="aebd5-117">Эти свойства используются в сочетании с свойствами **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)и **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)при обращении к сообщениям.</span><span class="sxs-lookup"><span data-stu-id="aebd5-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="aebd5-118">Формат строки квалифицирован **PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="aebd5-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="aebd5-119">Допустимые значения для этого свойства:</span><span class="sxs-lookup"><span data-stu-id="aebd5-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="aebd5-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aebd5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aebd5-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="aebd5-121">Protocol specifications</span></span>

<span data-ttu-id="aebd5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aebd5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aebd5-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="aebd5-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aebd5-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aebd5-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aebd5-125">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aebd5-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="aebd5-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aebd5-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aebd5-127">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="aebd5-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aebd5-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="aebd5-128">Header files</span></span>

<span data-ttu-id="aebd5-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aebd5-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="aebd5-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="aebd5-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="aebd5-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aebd5-131">Mapitags.h</span></span>
  
> <span data-ttu-id="aebd5-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="aebd5-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aebd5-133">См. также</span><span class="sxs-lookup"><span data-stu-id="aebd5-133">See also</span></span>



[<span data-ttu-id="aebd5-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aebd5-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aebd5-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="aebd5-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aebd5-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="aebd5-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aebd5-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="aebd5-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

