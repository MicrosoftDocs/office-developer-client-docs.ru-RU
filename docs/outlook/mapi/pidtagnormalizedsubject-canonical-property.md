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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329276"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="c1184-103">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="c1184-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="c1184-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1184-105">Содержит тему сообщения с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="c1184-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1184-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c1184-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1184-107">ПР_НОРМАЛИЗЕД_СУБЖЕКТ, ПР_НОРМАЛИЗЕД_СУБЖЕКТ_А, ПР_НОРМАЛИЗЕД_СУБЖЕКТ_В</span><span class="sxs-lookup"><span data-stu-id="c1184-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="c1184-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c1184-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1184-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="c1184-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="c1184-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c1184-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1184-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="c1184-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c1184-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c1184-112">Area:</span></span>  <br/> |<span data-ttu-id="c1184-113">Email</span><span class="sxs-lookup"><span data-stu-id="c1184-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1184-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1184-114">Remarks</span></span>

<span data-ttu-id="c1184-115">Эти свойства рассчитываются по хранилищу сообщений или поставщикам транспорта из свойств **пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md)) и **пр_субжект_префикс** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c1184-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="c1184-116">Если **пр_субжект_префикс** присутствует и является начальной подстрокой **пр_субжект**, **пр_нормализед_субжект** и связанным свойствам задаются содержимое **пр_субжект** с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="c1184-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="c1184-117">Если присутствует **пр_субжект_префикс** , но это не начальная подстрока **пр_субжект**, **пр_субжект_префикс** удаляется и пересчитывается из **пр_субжект** с использованием следующего правила: if String, содержащегося в **пр_субжект** начинается с одного до трех нецифровых символов, за которыми следует двоеточие и пробел, а строка вместе с двоеточием и пустым значением — префиксом.</span><span class="sxs-lookup"><span data-stu-id="c1184-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="c1184-118">Цифры, пробелы и знаки пунктуации являются недопустимыми префиксными символами.</span><span class="sxs-lookup"><span data-stu-id="c1184-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="c1184-119">Если **пр_субжект_префикс** отсутствует, он рассчитывается из **пр_субжект** с использованием правила, описанного в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="c1184-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="c1184-120">Затем этому свойству присваивается содержимое **пр_субжект** с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="c1184-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="c1184-121">**Note (Примечание** ) Когда **пр_субжект_префикс** — пустая строка, **пр_субжект** и это свойство одинаковы.</span><span class="sxs-lookup"><span data-stu-id="c1184-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="c1184-122">Конечно, это свойство должно быть частью **пр_субжект** , следующей за префиксом.</span><span class="sxs-lookup"><span data-stu-id="c1184-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="c1184-123">Если префикс отсутствует, это свойство становится таким же, как и **пр_субжект**.</span><span class="sxs-lookup"><span data-stu-id="c1184-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="c1184-124">**Пр_субжект_префикс** , и это свойство необходимо вычислить как часть реализации [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="c1184-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="c1184-125">Клиентское приложение не должно запрашивать метод [IMAPIProp::](imapiprop-getprops.md) /PROPS для их значений до тех пор, пока они не будут зафиксированы вызовом **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="c1184-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="c1184-126">В свойствах subject обычно используются небольшие строки менее 256 символов, а поставщик хранилища сообщений не обязан поддерживать интерфейс OLE **IStream** для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="c1184-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="c1184-127">Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** , а в \*\*\*\* случае возврата мапи_е_нот_енаугх_мемори — только при возвращении.</span><span class="sxs-lookup"><span data-stu-id="c1184-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c1184-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c1184-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1184-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c1184-129">Protocol specifications</span></span>

<span data-ttu-id="c1184-130">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1184-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1184-131">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c1184-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1184-132">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1184-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1184-133">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="c1184-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c1184-134">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1184-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1184-135">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="c1184-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1184-136">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="c1184-136">Header files</span></span>

<span data-ttu-id="c1184-137">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c1184-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1184-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c1184-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1184-139">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c1184-139">Mapitags.h</span></span>
  
> <span data-ttu-id="c1184-140">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c1184-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1184-141">См. также</span><span class="sxs-lookup"><span data-stu-id="c1184-141">See also</span></span>



[<span data-ttu-id="c1184-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c1184-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1184-143">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c1184-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1184-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c1184-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1184-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c1184-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

