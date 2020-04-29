---
title: Каноническое свойство PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339230"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="4d3c8-103">Каноническое свойство PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="4d3c8-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="4d3c8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d3c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d3c8-105">Содержит префикс темы, который обычно указывает на некоторые действия с сообщением, например "FW:" для переадресации.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d3c8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4d3c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d3c8-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="4d3c8-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="4d3c8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4d3c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d3c8-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="4d3c8-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="4d3c8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4d3c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d3c8-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d3c8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d3c8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4d3c8-112">Area:</span></span>  <br/> |<span data-ttu-id="4d3c8-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="4d3c8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d3c8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d3c8-114">Remarks</span></span>

<span data-ttu-id="4d3c8-115">Эти свойства рекомендуются для всех объектов Message.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="4d3c8-116">Префикс темы состоит из одного или нескольких буквенно-цифровых символов, за которыми следует двоеточие и пробел (часть префикса).</span><span class="sxs-lookup"><span data-stu-id="4d3c8-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="4d3c8-117">Он не должен содержать небуквенно-цифровых символов перед двоеточием.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="4d3c8-118">Отсутствие префикса может быть представлено пустой строкой или это свойство не задается.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="4d3c8-119">Если эти свойства заданы явно, строка может иметь любую длину и использовать любые буквенно-цифровые символы, но она должна соответствовать подстроке в начале свойства **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4d3c8-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="4d3c8-120">Если эти свойства не заданы отправителем и должны быть вычислены, их содержимое будет более ограниченным.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="4d3c8-121">Правило для вычисления префикса состоит в том, что **PR_SUBJECT** должен начинаться с одной, двух или трех букв (только алфавит), за которыми следует двоеточие и пробел.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="4d3c8-122">Если такая подстрока найдена в начале **PR_SUBJECT**, она становится строкой для этих свойств (а также остается в начале **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="4d3c8-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="4d3c8-123">В противном случае эти свойства будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="4d3c8-124">Эти свойства и **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) должны вычисляться как часть реализации [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="4d3c8-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="4d3c8-125">Клиент не должен запрашивать [IMAPIProp::/PROPS](imapiprop-getprops.md) для их значений до тех пор, пока они не будут зафиксированы вызовом **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="4d3c8-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="4d3c8-126">В свойствах subject обычно используются небольшие строки менее 256 символов, а поставщик хранилища сообщений не обязан поддерживать интерфейс OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="4d3c8-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="4d3c8-127">Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** , а затем последовательно прибегнуть к **IStream** , только если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="4d3c8-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d3c8-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d3c8-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d3c8-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4d3c8-129">Protocol specifications</span></span>

<span data-ttu-id="4d3c8-130">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d3c8-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d3c8-131">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d3c8-132">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d3c8-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d3c8-133">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4d3c8-134">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d3c8-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d3c8-135">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d3c8-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4d3c8-136">Header files</span></span>

<span data-ttu-id="4d3c8-137">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4d3c8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d3c8-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d3c8-139">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4d3c8-139">Mapitags.h</span></span>
  
> <span data-ttu-id="4d3c8-140">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4d3c8-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d3c8-141">См. также</span><span class="sxs-lookup"><span data-stu-id="4d3c8-141">See also</span></span>



[<span data-ttu-id="4d3c8-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4d3c8-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d3c8-143">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4d3c8-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d3c8-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4d3c8-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d3c8-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4d3c8-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

