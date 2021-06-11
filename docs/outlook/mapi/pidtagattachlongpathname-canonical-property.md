---
title: Каноническое свойство PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339370"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="7d0f3-103">Каноническое свойство PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="7d0f3-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="7d0f3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d0f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d0f3-105">Содержит полностью квалифицированный длинный путь вложения и имя файла.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d0f3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7d0f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d0f3-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="7d0f3-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="7d0f3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7d0f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d0f3-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="7d0f3-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="7d0f3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7d0f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d0f3-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d0f3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7d0f3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7d0f3-112">Area:</span></span>  <br/> |<span data-ttu-id="7d0f3-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="7d0f3-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d0f3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d0f3-114">Remarks</span></span>

<span data-ttu-id="7d0f3-115">Эти свойства применимы при использовании значений свойств **PR_ATTACH_METHOD** [(PidTagAttachMethod),](pidtagattachmethod-canonical-property.md)которые указывают на вложение по ссылке: **ATTACH_BY_REFERENCE,** **ATTACH_BY_REF_RESOLVE** или **ATTACH_BY_REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="7d0f3-116">Платформы, поддерживающие длинные имена **файлов,** должны задать как PR_ATTACH_LONG_PATHNAME, так и связанные свойства и **свойства PR_ATTACH_PATHNAME** [(PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)при отправке, **и** должны сначала проверять PR_ATTACH_LONG_PATHNAME или связанные свойства при получении.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="7d0f3-117">Клиентский приложение должно настроить эти свойства на предложенный длинный путь и имя файла, которые будут использоваться, если хост-машина, получающая сообщение, поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="7d0f3-118">Настройка этих свойств указывает на то, что данные вложения не включены в сообщение, но доступны на общем файловом сервере.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="7d0f3-119">В отличие от каталогов и **имен** файлов, предоставляемых PR_ATTACH_PATHNAME, эти каталоги и имена файлов не ограничиваются восьмилиманным каталогом или файловым именом плюс расширением на три символа.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="7d0f3-120">Вместо этого каждый каталог или имя файла может иметь длину до 256 символов, включая период имени, расширения и сепаратора.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="7d0f3-121">Однако общий путь ограничен 256 символами.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="7d0f3-122">Клиенты должны использовать универсальную конвенцию именования (UNC) в большинстве случаев, когда файл является общим, и должны использовать абсолютный путь, когда файл локальный.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="7d0f3-123">MAPI работает только с путями и именами файлов в наборе символов ANSI.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="7d0f3-124">Клиентские приложения, которые используют пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d0f3-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7d0f3-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d0f3-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7d0f3-126">Protocol specifications</span></span>

<span data-ttu-id="7d0f3-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d0f3-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d0f3-128">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7d0f3-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d0f3-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d0f3-130">Указывает свойства зашифрованных сообщений с управляемым правами.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d0f3-131">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="7d0f3-131">Header files</span></span>

<span data-ttu-id="7d0f3-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d0f3-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d0f3-133">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d0f3-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d0f3-134">Mapitags.h</span></span>
  
> <span data-ttu-id="7d0f3-135">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7d0f3-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d0f3-136">См. также</span><span class="sxs-lookup"><span data-stu-id="7d0f3-136">See also</span></span>



[<span data-ttu-id="7d0f3-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0f3-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d0f3-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0f3-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d0f3-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0f3-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d0f3-140">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="7d0f3-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

