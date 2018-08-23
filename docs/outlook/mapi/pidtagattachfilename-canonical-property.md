---
title: Каноническое свойство PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c5354618383a97b362348b14aea174d6f2266d6c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583283"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="2709a-103">Каноническое свойство PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="2709a-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="2709a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2709a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2709a-105">Содержит имя базового файла и расширение, исключая путь вложения.</span><span class="sxs-lookup"><span data-stu-id="2709a-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2709a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2709a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2709a-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="2709a-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="2709a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2709a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2709a-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="2709a-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="2709a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2709a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2709a-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2709a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2709a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2709a-112">Area:</span></span>  <br/> |<span data-ttu-id="2709a-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="2709a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2709a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2709a-114">Remarks</span></span>

<span data-ttu-id="2709a-115">Рекомендуется, что объекты вложения предоставлять эти свойства, которые относятся к значениям **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**и **ATTACH_BY_REF_ONLY** **PR_ATTACH_METHOD** Свойство ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2709a-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="2709a-116">Связанные свойства и **PR_ATTACH_FILENAME** необходимы, когда используется одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2709a-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="2709a-117">Эти свойства можно использовать в качестве предлагаемого имени файла для сохранения вложения и добавьте расширение имени файла, если свойство **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) не указан.</span><span class="sxs-lookup"><span data-stu-id="2709a-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="2709a-118">Имя файла ограничен восемь символов, а также расширения-трех символов.</span><span class="sxs-lookup"><span data-stu-id="2709a-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="2709a-119">Платформа, которая поддерживает длинные имена файлов задайте это свойство и свойство **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2709a-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="2709a-120">MAPI для работы только с имена файлов и другие строки, переданным в него, в наборе символов American National стандартов института (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2709a-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="2709a-121">Клиентские приложения, использующие имена файлов в набор символов (ПВТ) необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="2709a-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2709a-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2709a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2709a-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2709a-123">Protocol specifications</span></span>

<span data-ttu-id="2709a-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2709a-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2709a-125">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="2709a-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2709a-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2709a-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2709a-127">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="2709a-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="2709a-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2709a-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2709a-129">Задает свойства управляемый правами закодированный сообщений.</span><span class="sxs-lookup"><span data-stu-id="2709a-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="2709a-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2709a-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2709a-131">Указывает, подписанной и зашифрованной свойства сообщений S/MIME.</span><span class="sxs-lookup"><span data-stu-id="2709a-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="2709a-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2709a-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2709a-133">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="2709a-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2709a-134">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2709a-134">Header files</span></span>

<span data-ttu-id="2709a-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2709a-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="2709a-136">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2709a-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="2709a-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2709a-137">Mapitags.h</span></span>
  
> <span data-ttu-id="2709a-138">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2709a-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2709a-139">См. также</span><span class="sxs-lookup"><span data-stu-id="2709a-139">See also</span></span>



[<span data-ttu-id="2709a-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2709a-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2709a-141">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2709a-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2709a-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2709a-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2709a-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2709a-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

