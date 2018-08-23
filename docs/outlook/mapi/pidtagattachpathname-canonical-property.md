---
title: Каноническое свойство PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: add85bbf9c7608434be045bc30a11b8a28ccaa1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578411"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="48a07-103">Каноническое свойство PidTagAttachPathname</span><span class="sxs-lookup"><span data-stu-id="48a07-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="48a07-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48a07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48a07-105">Содержит полный путь и имя файла вложения.</span><span class="sxs-lookup"><span data-stu-id="48a07-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48a07-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="48a07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48a07-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="48a07-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="48a07-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="48a07-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48a07-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="48a07-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="48a07-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="48a07-110">Data type:</span></span>  <br/> |<span data-ttu-id="48a07-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="48a07-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="48a07-112">Область:</span><span class="sxs-lookup"><span data-stu-id="48a07-112">Area:</span></span>  <br/> |<span data-ttu-id="48a07-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="48a07-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48a07-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="48a07-114">Remarks</span></span>

<span data-ttu-id="48a07-115">Рекомендуется, что вложения вложенных предоставлять эти свойства.</span><span class="sxs-lookup"><span data-stu-id="48a07-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="48a07-116">Установки значения указывает, что данные вложения не включена в сообщение, но доступны в распространенных файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="48a07-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="48a07-117">Эти свойства требуются в сочетании с любым флаги **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), которые указывают вложения по ссылке: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**или **ATTACH_BY_REF_ ТОЛЬКО**.</span><span class="sxs-lookup"><span data-stu-id="48a07-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="48a07-118">Каждый каталог или имя файла ограничен имени восьми символов, а также расширения-трех символов.</span><span class="sxs-lookup"><span data-stu-id="48a07-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="48a07-119">Общий путь ограничен до 256 символов.</span><span class="sxs-lookup"><span data-stu-id="48a07-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="48a07-120">Платформа, которая поддерживает длинные имена файлов задайте оба этих свойств и **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48a07-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="48a07-121">Клиентские приложения следует использовать универсальное соглашение об именах (UNC) в большинстве случаев, когда файл является общей и следует использовать абсолютный путь, если файл является локальным.</span><span class="sxs-lookup"><span data-stu-id="48a07-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="48a07-122">MAPI для работы только с пути и имена файлов в формате ANSI набор знаков.</span><span class="sxs-lookup"><span data-stu-id="48a07-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="48a07-123">Клиенты, использующие пути и имена файлов в набор символов OEM необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="48a07-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48a07-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="48a07-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48a07-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="48a07-125">Protocol specifications</span></span>

<span data-ttu-id="48a07-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48a07-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48a07-127">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="48a07-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="48a07-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48a07-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48a07-129">Задает свойства управляемый правами закодированный сообщений.</span><span class="sxs-lookup"><span data-stu-id="48a07-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48a07-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="48a07-130">Header files</span></span>

<span data-ttu-id="48a07-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48a07-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="48a07-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="48a07-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="48a07-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48a07-133">Mapitags.h</span></span>
  
> <span data-ttu-id="48a07-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="48a07-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48a07-135">См. также</span><span class="sxs-lookup"><span data-stu-id="48a07-135">See also</span></span>



[<span data-ttu-id="48a07-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="48a07-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="48a07-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="48a07-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="48a07-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48a07-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48a07-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48a07-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48a07-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="48a07-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48a07-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="48a07-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

