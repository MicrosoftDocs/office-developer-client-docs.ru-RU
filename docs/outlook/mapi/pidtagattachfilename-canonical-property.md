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
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319224"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="64e63-103">Каноническое свойство PidTagAttachFilename</span><span class="sxs-lookup"><span data-stu-id="64e63-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="64e63-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64e63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64e63-105">Содержит базовое имя и расширение файла вложения, исключая путь.</span><span class="sxs-lookup"><span data-stu-id="64e63-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64e63-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="64e63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64e63-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="64e63-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="64e63-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="64e63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64e63-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="64e63-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="64e63-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="64e63-110">Data type:</span></span>  <br/> |<span data-ttu-id="64e63-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="64e63-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="64e63-112">Область:</span><span class="sxs-lookup"><span data-stu-id="64e63-112">Area:</span></span>  <br/> |<span data-ttu-id="64e63-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="64e63-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64e63-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="64e63-114">Remarks</span></span>

<span data-ttu-id="64e63-115">Рекомендуется, чтобы объекты вложения подвергали эти свойства, относящиеся к свойству **ATTACH_BY_VALUE,** **ATTACH_BY_REFERENCE,** **ATTACH_BY_REF_RESOLVE** и  **ATTACH_BY_REF_ONLY** значений PR_ATTACH_METHOD [(PidTagAttachMethod).](pidtagattachmethod-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="64e63-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="64e63-116">**PR_ATTACH_FILENAME** и связанные свойства необходимы при любом из этих значений.</span><span class="sxs-lookup"><span data-stu-id="64e63-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="64e63-117">Эти свойства можно использовать в качестве предложенного имени файла для сохранения вложения и для обеспечения расширения имени **файла,** если свойство [PR_ATTACH_EXTENSION (PidTagAttachExtension)](pidtagattachextension-canonical-property.md)не предоставлено.</span><span class="sxs-lookup"><span data-stu-id="64e63-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="64e63-118">Имя файла ограничено восемью символами, а также расширением с тремя символами.</span><span class="sxs-lookup"><span data-stu-id="64e63-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="64e63-119">Для платформы с длинными именами файлов установите как это **свойство,** так и PR_ATTACH_LONG_FILENAME [(PidTagAttachLongFilename).](pidtagattachlongfilename-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="64e63-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="64e63-120">MAPI работает только с именами файлов и другими строками, переданными ему, в наборе символов Американского института национальных стандартов (ANSI).</span><span class="sxs-lookup"><span data-stu-id="64e63-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="64e63-121">Клиентские приложения, которые используют имена файлов в исходном наборе символов производителя оборудования (OEM), должны преобразовать их в ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="64e63-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="64e63-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="64e63-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64e63-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="64e63-123">Protocol specifications</span></span>

<span data-ttu-id="64e63-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64e63-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64e63-125">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="64e63-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="64e63-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64e63-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64e63-127">Преобразуется из стандартных конвенций электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="64e63-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="64e63-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64e63-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64e63-129">Указывает свойства зашифрованных сообщений с управляемым правами.</span><span class="sxs-lookup"><span data-stu-id="64e63-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="64e63-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64e63-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64e63-131">Указывает свойства подписанных и зашифрованных сообщений S/MIME.</span><span class="sxs-lookup"><span data-stu-id="64e63-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="64e63-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64e63-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64e63-133">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="64e63-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64e63-134">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="64e63-134">Header files</span></span>

<span data-ttu-id="64e63-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64e63-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="64e63-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="64e63-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="64e63-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64e63-137">Mapitags.h</span></span>
  
> <span data-ttu-id="64e63-138">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="64e63-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64e63-139">См. также</span><span class="sxs-lookup"><span data-stu-id="64e63-139">See also</span></span>



[<span data-ttu-id="64e63-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64e63-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64e63-141">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64e63-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64e63-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="64e63-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64e63-143">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="64e63-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

