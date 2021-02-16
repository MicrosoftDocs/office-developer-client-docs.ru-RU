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
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="781b4-103">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="781b4-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="781b4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="781b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="781b4-105">Содержит тему сообщения с удаляемой префиксом.</span><span class="sxs-lookup"><span data-stu-id="781b4-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="781b4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="781b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="781b4-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="781b4-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="781b4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="781b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="781b4-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="781b4-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="781b4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="781b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="781b4-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="781b4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="781b4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="781b4-112">Area:</span></span>  <br/> |<span data-ttu-id="781b4-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="781b4-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="781b4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="781b4-114">Remarks</span></span>

<span data-ttu-id="781b4-115">Эти свойства вычисляются хранилищем сообщений или поставщиками транспорта из свойств **PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)и **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md)следующим образом.</span><span class="sxs-lookup"><span data-stu-id="781b4-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="781b4-116">Если  PR_SUBJECT_PREFIX присутствует и является начальной подстрока **PR_SUBJECT,**  PR_NORMALIZED_SUBJECT и связанные свойства устанавливаются на содержимое  PR_SUBJECT с префиксом удален.</span><span class="sxs-lookup"><span data-stu-id="781b4-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="781b4-117">Если **PR_SUBJECT_PREFIX** присутствует, но не является начальной подстрокой **PR_SUBJECT,** **PR_SUBJECT_PREFIX** удаляется и пересчитываются из **PR_SUBJECT** с помощью следующего правила: если строка в **PR_SUBJECT** начинается с одного или трех нечислических символов, за которыми следуют двоеточие и пробел, строка вместе с двоеточием и пустым становится префиксом.</span><span class="sxs-lookup"><span data-stu-id="781b4-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="781b4-118">Цифры, пустые символы и знаки препинания не являются допустимыми символами префикса.</span><span class="sxs-lookup"><span data-stu-id="781b4-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="781b4-119">Если **PR_SUBJECT_PREFIX** нет, он вычисляется из  PR_SUBJECT с помощью правила, описанного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="781b4-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="781b4-120">Затем этому свойству устанавливается содержимое PR_SUBJECT **с** удаляемым префиксом.</span><span class="sxs-lookup"><span data-stu-id="781b4-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="781b4-121">**Примечание** Если **PR_SUBJECT_PREFIX** пустая **строка,** PR_SUBJECT это свойство будет одинаковым.</span><span class="sxs-lookup"><span data-stu-id="781b4-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="781b4-122">В конечном счете это свойство должно быть **частью** PR_SUBJECT после префикса.</span><span class="sxs-lookup"><span data-stu-id="781b4-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="781b4-123">Если префикса нет, это свойство становится таким же, **как PR_SUBJECT.**</span><span class="sxs-lookup"><span data-stu-id="781b4-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="781b4-124">**PR_SUBJECT_PREFIX** и это свойство должно быть вычислено в рамках [реализации IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="781b4-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="781b4-125">Клиентские приложения не должны запросить у метода [IMAPIProp::GetProps](imapiprop-getprops.md) их значения, пока они не будут зафиксированы вызовом **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="781b4-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="781b4-126">Свойства темы, как правило, являются небольшими строками менее 256 символов, и поставщик хранилище сообщений не обязан поддерживать интерфейс **IStream** для связывания и встраиния объектов (OLE).</span><span class="sxs-lookup"><span data-stu-id="781b4-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="781b4-127">Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** и использовать **IStream,** только если MAPI_E_NOT_ENOUGH_MEMORY возвращается.</span><span class="sxs-lookup"><span data-stu-id="781b4-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="781b4-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="781b4-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="781b4-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="781b4-129">Protocol specifications</span></span>

<span data-ttu-id="781b4-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="781b4-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="781b4-131">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="781b4-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="781b4-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="781b4-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="781b4-133">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="781b4-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="781b4-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="781b4-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="781b4-135">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="781b4-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="781b4-136">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="781b4-136">Header files</span></span>

<span data-ttu-id="781b4-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="781b4-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="781b4-138">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="781b4-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="781b4-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="781b4-139">Mapitags.h</span></span>
  
> <span data-ttu-id="781b4-140">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="781b4-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="781b4-141">См. также</span><span class="sxs-lookup"><span data-stu-id="781b4-141">See also</span></span>



[<span data-ttu-id="781b4-142">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="781b4-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="781b4-143">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="781b4-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="781b4-144">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="781b4-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="781b4-145">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="781b4-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

