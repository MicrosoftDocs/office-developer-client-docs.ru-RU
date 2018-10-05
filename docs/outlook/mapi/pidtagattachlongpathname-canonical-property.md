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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383109"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="7adc4-103">Каноническое свойство PidTagAttachLongPathname</span><span class="sxs-lookup"><span data-stu-id="7adc4-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="7adc4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7adc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7adc4-105">Содержит полное длинный путь и имя файла вложения.</span><span class="sxs-lookup"><span data-stu-id="7adc4-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7adc4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7adc4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7adc4-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="7adc4-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="7adc4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7adc4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7adc4-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="7adc4-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="7adc4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7adc4-110">Data type:</span></span>  <br/> |<span data-ttu-id="7adc4-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7adc4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7adc4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7adc4-112">Area:</span></span>  <br/> |<span data-ttu-id="7adc4-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="7adc4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7adc4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7adc4-114">Remarks</span></span>

<span data-ttu-id="7adc4-115">Эти свойства могут быть применены при использовании значения свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), которые указывают вложений с помощью ссылки: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**или **ATTACH_BY _REF_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="7adc4-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="7adc4-116">Платформы, поддерживающие длинные имена файлов следует устанавливать **PR_ATTACH_LONG_PATHNAME** или связанные свойства и свойства **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) при отправке и должен проверить, \*\*PR_ATTACH_LONG_PATHNAME \*\*или сначала связанные свойства при приеме.</span><span class="sxs-lookup"><span data-stu-id="7adc4-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="7adc4-117">Клиентское приложение следует задать эти свойства предложенного длинный путь и имя файла для использования в том случае, если компьютер, появления сообщения об ошибке поддерживает длинные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="7adc4-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="7adc4-118">Установка этих свойств указывает, что данные вложения не включена в сообщение, но доступны в распространенных файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="7adc4-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="7adc4-119">В отличие от предоставлено **PR_ATTACH_PATHNAME**имен файлов и папок эти имен файлов и папок, не ограничены восьми символов каталог или имя файла, а также расширения-трех символов.</span><span class="sxs-lookup"><span data-stu-id="7adc4-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="7adc4-120">Вместо этого каждого каталог или имя файла может быть длиной до 256 символов, включая имя, расширение и разделителя групп разрядов периода.</span><span class="sxs-lookup"><span data-stu-id="7adc4-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="7adc4-121">Тем не менее общий путь — это более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="7adc4-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="7adc4-122">Клиенты должны использовать универсальное соглашение об именах (UNC) в большинстве случаев при файл является общей и следует использовать абсолютный путь, когда локальный файл.</span><span class="sxs-lookup"><span data-stu-id="7adc4-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="7adc4-123">MAPI для работы только с пути и имена файлов в формате ANSI набор знаков.</span><span class="sxs-lookup"><span data-stu-id="7adc4-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="7adc4-124">Клиентские приложения, использующие пути и имена файлов в кодировке OEM необходимо преобразовать их в формате ANSI перед вызовом MAPI.</span><span class="sxs-lookup"><span data-stu-id="7adc4-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7adc4-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7adc4-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7adc4-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7adc4-126">Protocol specifications</span></span>

<span data-ttu-id="7adc4-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7adc4-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7adc4-128">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="7adc4-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7adc4-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7adc4-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7adc4-130">Задает свойства управляемый правами закодированный сообщений.</span><span class="sxs-lookup"><span data-stu-id="7adc4-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7adc4-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7adc4-131">Header files</span></span>

<span data-ttu-id="7adc4-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7adc4-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="7adc4-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7adc4-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="7adc4-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7adc4-134">Mapitags.h</span></span>
  
> <span data-ttu-id="7adc4-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7adc4-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7adc4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="7adc4-136">See also</span></span>



[<span data-ttu-id="7adc4-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7adc4-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7adc4-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7adc4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7adc4-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7adc4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7adc4-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7adc4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

