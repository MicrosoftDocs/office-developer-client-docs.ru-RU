---
title: Каноническое свойство PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339328"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="164b1-103">Каноническое свойство PidTagAttachLongFilename</span><span class="sxs-lookup"><span data-stu-id="164b1-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="164b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="164b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="164b1-105">Содержит длинное имя файла и расширение вложения, за исключением пути.</span><span class="sxs-lookup"><span data-stu-id="164b1-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="164b1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="164b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="164b1-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="164b1-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="164b1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="164b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="164b1-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="164b1-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="164b1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="164b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="164b1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="164b1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="164b1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="164b1-112">Area:</span></span>  <br/> |<span data-ttu-id="164b1-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="164b1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="164b1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="164b1-114">Remarks</span></span>

<span data-ttu-id="164b1-115">Эти свойства относятся к значениям ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE и ATTACH_BY_REF_ONLY свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod).](pidtagattachmethod-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="164b1-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="164b1-116">Платформы, поддерживающие длинные имена файлов, должны устанавливать свойства **PR_ATTACH_LONG_FILENAME** и **PR_ATTACH_FILENAME** ([PidTagAttachFilename)](pidtagattachfilename-canonical-property.md)  при отправке и проверять PR_ATTACH_LONG_FILENAME при получении.</span><span class="sxs-lookup"><span data-stu-id="164b1-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="164b1-117">Клиентские приложения должны установить для этого свойства рекомендуемый длинный файл, который будет использоваться, если хост-компьютер, получающий сообщение, поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="164b1-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="164b1-118">**PR_ATTACH_LONG_FILENAME** можно использовать в качестве имени файла для сохранения вложения и для обеспечения расширения имени файла, если свойство **PR_ATTACH_EXTENSION** ([PidTagAttachExtension)](pidtagattachextension-canonical-property.md)не предоставлено.</span><span class="sxs-lookup"><span data-stu-id="164b1-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="164b1-119">В отличие от имени файла, предоставленного **PR_ATTACH_FILENAME,** это имя не ограничивается восемью символами и трех символьным расширением.</span><span class="sxs-lookup"><span data-stu-id="164b1-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="164b1-120">Вместо этого он может иметь длину до 256 символов, включая имя файла, расширение и период сепаратора.</span><span class="sxs-lookup"><span data-stu-id="164b1-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="164b1-121">MAPI работает только с именами файлов в наборе символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="164b1-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="164b1-122">Клиентские приложения, которые используют имена файлов в наборе символов OEM, должны преобразовывать их в ANSI, прежде чем вызывать MAPI.</span><span class="sxs-lookup"><span data-stu-id="164b1-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="164b1-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="164b1-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="164b1-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="164b1-124">Protocol specifications</span></span>

<span data-ttu-id="164b1-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164b1-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164b1-126">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="164b1-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="164b1-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164b1-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164b1-128">Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="164b1-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="164b1-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164b1-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164b1-130">Указывает свойства сообщений в кодированной кодировки с управлением правами.</span><span class="sxs-lookup"><span data-stu-id="164b1-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="164b1-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="164b1-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="164b1-132">Указывает свойства и операции, которые разрешены для представления голосовой почты и факсимили.</span><span class="sxs-lookup"><span data-stu-id="164b1-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="164b1-133">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="164b1-133">Header files</span></span>

<span data-ttu-id="164b1-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="164b1-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="164b1-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="164b1-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="164b1-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="164b1-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="164b1-137">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="164b1-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="164b1-138">См. также</span><span class="sxs-lookup"><span data-stu-id="164b1-138">See also</span></span>



[<span data-ttu-id="164b1-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="164b1-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="164b1-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="164b1-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="164b1-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="164b1-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="164b1-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="164b1-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

