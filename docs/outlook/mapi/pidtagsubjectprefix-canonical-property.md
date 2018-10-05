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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385650"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="41453-103">Каноническое свойство PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="41453-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="41453-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41453-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41453-105">Содержит префикс темы, который указывает на то, какие-либо действия в окне сообщения, например, «по: "для пересылки.</span><span class="sxs-lookup"><span data-stu-id="41453-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41453-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="41453-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41453-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="41453-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="41453-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="41453-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41453-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="41453-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="41453-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="41453-110">Data type:</span></span>  <br/> |<span data-ttu-id="41453-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="41453-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="41453-112">Область:</span><span class="sxs-lookup"><span data-stu-id="41453-112">Area:</span></span>  <br/> |<span data-ttu-id="41453-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="41453-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41453-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="41453-114">Remarks</span></span>

<span data-ttu-id="41453-115">Эти свойства, рекомендуется использовать для всех объектов сообщения.</span><span class="sxs-lookup"><span data-stu-id="41453-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="41453-116">Префикс Тема состоит из одного или нескольких буквенно-цифровых символов, за которым следует двоеточие и пробелом (который входят в состав префикс).</span><span class="sxs-lookup"><span data-stu-id="41453-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="41453-117">Не должно содержать все символы перед двоеточием.</span><span class="sxs-lookup"><span data-stu-id="41453-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="41453-118">Отсутствие префикса может быть представлена с пустой строке или это свойство не задано.</span><span class="sxs-lookup"><span data-stu-id="41453-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="41453-119">Если эти свойства задаются явно, строка может быть любой длины и использовать любой буквенно-цифровых символов, но он должен соответствовать подстроки в начале свойство **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="41453-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="41453-120">Если эти свойства не заданы отправителем и вычисляемые, их содержимое более ограничены.</span><span class="sxs-lookup"><span data-stu-id="41453-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="41453-121">— Это правило вычислений префикс, что **PR_SUBJECT** должен начинаться с один, два или три буквы (к буквам и цифрам только) за которым следует двоеточие и пробел.</span><span class="sxs-lookup"><span data-stu-id="41453-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="41453-122">При обнаружении таких подстроки в начале **PR_SUBJECT**его при этом становится строка для этих свойств (и не используется в начале **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="41453-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="41453-123">В противном случае эти свойства остаются неопределенные.</span><span class="sxs-lookup"><span data-stu-id="41453-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="41453-124">Эти свойства и **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) следует вычисляется как часть реализации [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="41453-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="41453-125">Клиент должен не запрашивать пользователя [IMAPIProp::GetProps](imapiprop-getprops.md) для их значения до их фиксации вызовом **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="41453-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="41453-126">Свойства темы — это обычно коротких строк менее 256 символов и поставщика хранилища сообщений не обязаны поддержки интерфейса OLE **IStream** на них.</span><span class="sxs-lookup"><span data-stu-id="41453-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="41453-127">Клиент должен всегда сначала попытаться доступ через интерфейс **IMAPIProp** и прибегать к **IStream** только в том случае, если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="41453-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="41453-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="41453-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41453-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="41453-129">Protocol specifications</span></span>

<span data-ttu-id="41453-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41453-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41453-131">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="41453-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41453-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41453-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41453-133">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="41453-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="41453-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41453-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41453-135">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="41453-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41453-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="41453-136">Header files</span></span>

<span data-ttu-id="41453-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41453-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="41453-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="41453-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="41453-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41453-139">Mapitags.h</span></span>
  
> <span data-ttu-id="41453-140">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="41453-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41453-141">См. также</span><span class="sxs-lookup"><span data-stu-id="41453-141">See also</span></span>



[<span data-ttu-id="41453-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="41453-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41453-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="41453-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41453-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="41453-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41453-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="41453-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

