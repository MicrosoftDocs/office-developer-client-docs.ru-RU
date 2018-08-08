---
title: Каноническое свойство PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Последнее изменение: 07 сентября 2016'
ms.openlocfilehash: 1720e9a2eeb54daed1e559f99b0c63ce09585419
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810873"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="5bd34-103">Каноническое свойство PidTagAttachMethod</span><span class="sxs-lookup"><span data-stu-id="5bd34-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="5bd34-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bd34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bd34-105">Содержит определенные MAPI константу, представляющее того, который может осуществляться содержимого вложения.</span><span class="sxs-lookup"><span data-stu-id="5bd34-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bd34-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5bd34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bd34-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="5bd34-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="5bd34-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5bd34-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5bd34-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="5bd34-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="5bd34-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5bd34-110">Data type:</span></span>  <br/> |<span data-ttu-id="5bd34-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5bd34-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5bd34-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5bd34-112">Area:</span></span>  <br/> |<span data-ttu-id="5bd34-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="5bd34-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bd34-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bd34-114">Remarks</span></span>

<span data-ttu-id="5bd34-115">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5bd34-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="5bd34-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="5bd34-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="5bd34-117">Вложение только что создано.</span><span class="sxs-lookup"><span data-stu-id="5bd34-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="5bd34-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="5bd34-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="5bd34-119">Свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) содержит данные вложения.</span><span class="sxs-lookup"><span data-stu-id="5bd34-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="5bd34-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="5bd34-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="5bd34-121">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) или свойство **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) содержит полный путь, идентифицирующий вложения получателям с доступом к общего файла сервер.</span><span class="sxs-lookup"><span data-stu-id="5bd34-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="5bd34-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="5bd34-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="5bd34-123">Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, идентифицирующий вложение.</span><span class="sxs-lookup"><span data-stu-id="5bd34-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="5bd34-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="5bd34-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="5bd34-125">Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, идентифицирующий вложение.</span><span class="sxs-lookup"><span data-stu-id="5bd34-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="5bd34-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="5bd34-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="5bd34-127">Свойство **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) содержит внедренный объект, который поддерживает интерфейс **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="5bd34-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="5bd34-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="5bd34-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="5bd34-129">Вложение представляет внедренный объект OLE.</span><span class="sxs-lookup"><span data-stu-id="5bd34-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="5bd34-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="5bd34-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="5bd34-131">Содержимое вложения не в сообщении.</span><span class="sxs-lookup"><span data-stu-id="5bd34-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="5bd34-132">При создании, вложения у каждого объекта есть начальное значение **PR_ATTACH_METHOD** **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="5bd34-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="5bd34-133">Клиентские приложения и поставщиков услуг только необходимых для поддержки метод вложения, представленный значением **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="5bd34-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="5bd34-134">Другие методы вложения являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="5bd34-134">The other attachment methods are optional.</span></span> <span data-ttu-id="5bd34-135">Хранилище сообщений не требует принудительного согласованность значение **PR_ATTACH_METHOD** и значения свойства вложения.</span><span class="sxs-lookup"><span data-stu-id="5bd34-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="5bd34-136">Для полные пути, которые можно использовать с **ATTACH_BY_REFERENCE** и **ATTACH_BY_REF_ONLY**рекомендуются универсальных имен именования соглашение (UNC).</span><span class="sxs-lookup"><span data-stu-id="5bd34-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="5bd34-137">С помощью **ATTACH_BY_REF_RESOLVE**абсолютный путь быстрее, так как диспетчер очереди MAPI преобразует вложения в **ATTACH_BY_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="5bd34-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="5bd34-138">Если значение **ATTACH_BY_REFERENCE** , **PR_ATTACH_DATA_BIN** должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="5bd34-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="5bd34-139">Исходящие шлюза можно преобразовать **ATTACH_BY_REFERENCE** вложения в **ATTACH_BY_VALUE** вложения, скопировав данные вложения в свойстве **PR_ATTACH_DATA_BIN** .</span><span class="sxs-lookup"><span data-stu-id="5bd34-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="5bd34-140">Если значение **ATTACH_BY_REF_RESOLVE** , **PR_ATTACH_DATA_BIN** должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="5bd34-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="5bd34-141">При отправке сообщения с вложением **ATTACH_BY_REF_RESOLVE** диспетчер очереди MAPI копирует данные вложения в **ATTACH_BY_VALUE** вложения.</span><span class="sxs-lookup"><span data-stu-id="5bd34-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="5bd34-142">Этот процесс разрешения помещает данные вложения в **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="5bd34-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="5bd34-143">Если значение **ATTACH_BY_REF_ONLY** , **PR_ATTACH_DATA_BIN** должна быть пустой и системы обмена сообщениями никогда не разрешает ссылку вложения.</span><span class="sxs-lookup"><span data-stu-id="5bd34-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="5bd34-144">Это значение используется, когда требуется отправить ссылку, но не данные.</span><span class="sxs-lookup"><span data-stu-id="5bd34-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="5bd34-145">Если объект OLE в формате OLE 2.0 **IStorage** , данных доступен через **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="5bd34-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="5bd34-146">Если объект OLE в формате OLE 1.0 **OLESTREAM** , данных доступен через **PR_ATTACH_DATA_BIN** как интерфейс **IStream**.</span><span class="sxs-lookup"><span data-stu-id="5bd34-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="5bd34-147">Можно определить тип кодировки OLE по значению **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5bd34-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="5bd34-148">Дополнительные сведения о интерфейсов OLE и форматы *OLE Справочник программиста* см.</span><span class="sxs-lookup"><span data-stu-id="5bd34-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5bd34-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bd34-149">Remarks</span></span>

<span data-ttu-id="5bd34-150">При **ATTACH_BY_WEBREFERENCE** **PR_ATTACH_METHOD** не является содержимое вложения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="5bd34-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="5bd34-151">Вместо этого свойство **PR_ATTACH_LONG_FILENAME** содержит абсолютный URL-адрес для содержимого вложения, которая хранится в Интернете.</span><span class="sxs-lookup"><span data-stu-id="5bd34-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5bd34-152">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bd34-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bd34-153">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5bd34-153">Protocol specifications</span></span>

<span data-ttu-id="5bd34-154">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bd34-154">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bd34-155">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="5bd34-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bd34-156">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5bd34-156">Header files</span></span>

<span data-ttu-id="5bd34-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bd34-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bd34-158">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5bd34-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="5bd34-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5bd34-159">Mapitags.h</span></span>
  
> <span data-ttu-id="5bd34-160">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5bd34-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bd34-161">См. также</span><span class="sxs-lookup"><span data-stu-id="5bd34-161">See also</span></span>



[<span data-ttu-id="5bd34-162">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="5bd34-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="5bd34-163">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bd34-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bd34-164">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bd34-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bd34-165">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5bd34-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bd34-166">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5bd34-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

