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
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327232"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="9edce-103">Каноническое свойство PidTagAttachPathname</span><span class="sxs-lookup"><span data-stu-id="9edce-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="9edce-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9edce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9edce-105">Содержит полный путь и имя файла вложения.</span><span class="sxs-lookup"><span data-stu-id="9edce-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9edce-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9edce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9edce-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="9edce-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="9edce-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9edce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9edce-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="9edce-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="9edce-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9edce-110">Data type:</span></span>  <br/> |<span data-ttu-id="9edce-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9edce-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9edce-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9edce-112">Area:</span></span>  <br/> |<span data-ttu-id="9edce-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="9edce-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9edce-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9edce-114">Remarks</span></span>

<span data-ttu-id="9edce-115">Рекомендуется предоставлять этим свойствам вложенные объекты вложений.</span><span class="sxs-lookup"><span data-stu-id="9edce-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="9edce-116">Их установка указывает на то, что данные вложения не включены в сообщение, но доступны на общем файловом сервере.</span><span class="sxs-lookup"><span data-stu-id="9edce-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="9edce-117">Эти свойства необходимы в сочетании с любыми флагами **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), которые указывают вложение по ссылке: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**или **ATTACH_BY_REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="9edce-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="9edce-118">Имя каждого каталога или имени файла ограничено восемью символами и расширением из трех символов.</span><span class="sxs-lookup"><span data-stu-id="9edce-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="9edce-119">Общий путь ограничен 256 символами.</span><span class="sxs-lookup"><span data-stu-id="9edce-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="9edce-120">Для платформы, поддерживающей длинные имена файлов, задайте оба этих свойства и **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9edce-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="9edce-121">Клиентские приложения должны использовать в большинстве случаев универсальное соглашение об именовании (UNC), если файл является общим, и использовать абсолютный путь, если файл является локальным.</span><span class="sxs-lookup"><span data-stu-id="9edce-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="9edce-122">MAPI работает только с путями и именами в наборе знаков ANSI.</span><span class="sxs-lookup"><span data-stu-id="9edce-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="9edce-123">Клиенты, использующие пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="9edce-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9edce-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9edce-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9edce-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9edce-125">Protocol specifications</span></span>

<span data-ttu-id="9edce-126">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9edce-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9edce-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="9edce-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9edce-128">[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9edce-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9edce-129">Задает свойства сообщений, закодированных с помощью управления правами.</span><span class="sxs-lookup"><span data-stu-id="9edce-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9edce-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9edce-130">Header files</span></span>

<span data-ttu-id="9edce-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9edce-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="9edce-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9edce-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="9edce-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9edce-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9edce-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="9edce-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9edce-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9edce-135">See also</span></span>



[<span data-ttu-id="9edce-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="9edce-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="9edce-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="9edce-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="9edce-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9edce-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9edce-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9edce-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9edce-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9edce-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9edce-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9edce-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

