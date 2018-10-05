---
title: Каноническое свойство PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393231"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="dd4f8-103">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="dd4f8-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="dd4f8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd4f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd4f8-105">Тема сообщения содержит с любой префикс удалены.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd4f8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dd4f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd4f8-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="dd4f8-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="dd4f8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dd4f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd4f8-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="dd4f8-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="dd4f8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dd4f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd4f8-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd4f8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dd4f8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dd4f8-112">Area:</span></span>  <br/> |<span data-ttu-id="dd4f8-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="dd4f8-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd4f8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd4f8-114">Remarks</span></span>

<span data-ttu-id="dd4f8-115">Эти свойства вычисляются с хранилищем сообщений или поставщиками из свойства **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) и **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) транспорта следующим образом.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="dd4f8-116">Если **PR_SUBJECT_PREFIX** этот параметр указан и совпадает с началом из **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** и связанные свойства устанавливаются содержимое **PR_SUBJECT** с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="dd4f8-117">Если **PR_SUBJECT_PREFIX** этот параметр указан, но не является первоначальной подстроки из **PR_SUBJECT**, **PR_SUBJECT_PREFIX** удаления и перерасчете из **PR_SUBJECT** с помощью следующее правило: Если строка содержатся в **PR_SUBJECT** начинается с один-три буквенные символы, за которым следует двоеточие и пробелами, вместе с двоеточием и пустой строки становится префикса.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="dd4f8-118">Символы чисел, пробелов и знаков препинания не допустимый префикс символов.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="dd4f8-119">Если **PR_SUBJECT_PREFIX** не существует, он вычисляется из **PR_SUBJECT** с помощью правила, описанные в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="dd4f8-120">Это свойство затем присваивается содержимое **PR_SUBJECT** с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="dd4f8-121">**Примечание** При **PR_SUBJECT_PREFIX** — это пустая строка, **PR_SUBJECT** и это свойство, совпадают.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="dd4f8-122">В конечном счете это свойство должно быть частью **PR_SUBJECT** следующий префикс.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="dd4f8-123">Если префикс отсутствует, это свойство становится таким же, как **PR_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="dd4f8-124">Как часть реализации [IMAPIProp::SaveChanges](imapiprop-savechanges.md) следует вычисляемые **PR_SUBJECT_PREFIX** и это свойство.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="dd4f8-125">Клиентское приложение не может запрашивать пользователя метод [IMAPIProp::GetProps](imapiprop-getprops.md) для их значения, пока они не зафиксированы вызовом **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="dd4f8-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="dd4f8-126">Свойства темы — это обычно коротких строк менее 256 символов и поставщика хранилища сообщений не обязаны поддерживают интерфейс объекта связывания и внедрения (OLE) **IStream** на них.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="dd4f8-127">Клиент должен всегда сначала попытаться доступ через интерфейс **IMAPIProp** и прибегать к **IStream** только в том случае, если возвращается MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dd4f8-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dd4f8-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd4f8-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dd4f8-129">Protocol specifications</span></span>

<span data-ttu-id="dd4f8-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd4f8-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd4f8-131">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd4f8-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd4f8-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd4f8-133">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="dd4f8-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd4f8-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd4f8-135">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd4f8-136">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dd4f8-136">Header files</span></span>

<span data-ttu-id="dd4f8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd4f8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd4f8-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd4f8-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dd4f8-139">Mapitags.h</span></span>
  
> <span data-ttu-id="dd4f8-140">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="dd4f8-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd4f8-141">См. также</span><span class="sxs-lookup"><span data-stu-id="dd4f8-141">See also</span></span>



[<span data-ttu-id="dd4f8-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dd4f8-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd4f8-143">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dd4f8-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd4f8-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dd4f8-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd4f8-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dd4f8-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

