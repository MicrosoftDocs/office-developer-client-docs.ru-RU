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
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="8c0ea-103">Каноническое свойство PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="8c0ea-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="8c0ea-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c0ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c0ea-105">Содержит полный путь и имя файла для вложения.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c0ea-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8c0ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c0ea-107">ПР_АТТАЧ_ЛОНГ_ПАСНАМЕ, ПР_АТТАЧ_ЛОНГ_ПАСНАМЕ_А, ПР_АТТАЧ_ЛОНГ_ПАСНАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="8c0ea-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="8c0ea-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8c0ea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c0ea-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="8c0ea-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="8c0ea-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8c0ea-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c0ea-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="8c0ea-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8c0ea-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8c0ea-112">Area:</span></span>  <br/> |<span data-ttu-id="8c0ea-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="8c0ea-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c0ea-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c0ea-114">Remarks</span></span>

<span data-ttu-id="8c0ea-115">Эти свойства применяются при использовании любого значения свойства **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), указывающего на вложение по ссылке: **аттач_би_референце**, **аттач_би_реф_ресолве**или **аттач_би _РЕФ_ОНЛИ**.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="8c0ea-116">Платформы, поддерживающие длинные имена файлов, должны устанавливать как **пр_аттач_лонг_паснаме** , так и связанные свойства и **пр_аттач_паснаме** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) при отправке, а также проверять \*\*пр_аттач_лонг_паснаме \*\*и связанные с ними свойства при получении.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="8c0ea-117">Клиентское приложение должно задать для этих свойств предложенный длинный путь и имя файла, который будет использоваться, если хостный компьютер, принимающий сообщение, поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="8c0ea-118">Задание этих свойств указывает на то, что данные вложения не включены в сообщение, но доступны на общем файловом сервере.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="8c0ea-119">В отличие от каталогов и имен файлов, предоставленных **пр_аттач_паснаме**, эти каталоги и имена файлов не ограничиваются каталогом из восьми символов, а имя файла и расширением из трех символов.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="8c0ea-120">Вместо этого длина имени каталога или имени файла может доставлять до 256 символов, в том числе имя, расширение и период разделения.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="8c0ea-121">Однако общий путь ограничен 256 символами.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="8c0ea-122">В большинстве случаев клиенты должны использовать соглашение об именовании (UNC), если файл является общим, и использовать абсолютный путь, если файл является локальным.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="8c0ea-123">MAPI работает только с путями и именами в наборе знаков ANSI.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="8c0ea-124">Клиентские приложения, использующие пути и имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8c0ea-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8c0ea-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c0ea-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8c0ea-126">Protocol specifications</span></span>

<span data-ttu-id="8c0ea-127">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c0ea-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c0ea-128">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8c0ea-129">[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c0ea-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c0ea-130">Задает свойства сообщений, закодированных с помощью управления правами.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c0ea-131">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8c0ea-131">Header files</span></span>

<span data-ttu-id="8c0ea-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8c0ea-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c0ea-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c0ea-134">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8c0ea-134">Mapitags.h</span></span>
  
> <span data-ttu-id="8c0ea-135">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c0ea-136">См. также</span><span class="sxs-lookup"><span data-stu-id="8c0ea-136">See also</span></span>



[<span data-ttu-id="8c0ea-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8c0ea-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c0ea-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8c0ea-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c0ea-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8c0ea-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c0ea-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8c0ea-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

