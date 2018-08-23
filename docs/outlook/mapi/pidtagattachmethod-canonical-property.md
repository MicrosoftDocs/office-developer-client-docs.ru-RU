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
ms.openlocfilehash: 697f7e8045ca198c2c10b9396f19cb2d7ce8346e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583654"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="17a44-103">Каноническое свойство PidTagAttachMethod</span><span class="sxs-lookup"><span data-stu-id="17a44-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="17a44-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17a44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17a44-105">Содержит определенные MAPI константу, представляющее того, который может осуществляться содержимого вложения.</span><span class="sxs-lookup"><span data-stu-id="17a44-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17a44-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="17a44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17a44-107">PR_ATTACH_METHOD</span><span class="sxs-lookup"><span data-stu-id="17a44-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="17a44-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="17a44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17a44-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="17a44-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="17a44-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="17a44-110">Data type:</span></span>  <br/> |<span data-ttu-id="17a44-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="17a44-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="17a44-112">Область:</span><span class="sxs-lookup"><span data-stu-id="17a44-112">Area:</span></span>  <br/> |<span data-ttu-id="17a44-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="17a44-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17a44-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="17a44-114">Remarks</span></span>

<span data-ttu-id="17a44-115">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="17a44-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="17a44-116">NO_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="17a44-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="17a44-117">Вложение только что создано.</span><span class="sxs-lookup"><span data-stu-id="17a44-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="17a44-118">ATTACH_BY_VALUE</span><span class="sxs-lookup"><span data-stu-id="17a44-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="17a44-119">Свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) содержит данные вложения.</span><span class="sxs-lookup"><span data-stu-id="17a44-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="17a44-120">ATTACH_BY_REFERENCE</span><span class="sxs-lookup"><span data-stu-id="17a44-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="17a44-121">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) или свойство **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) содержит полный путь, идентифицирующий вложения получателям с доступом к общего файла сервер.</span><span class="sxs-lookup"><span data-stu-id="17a44-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="17a44-122">ATTACH_BY_REF_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="17a44-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="17a44-123">Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, идентифицирующий вложение.</span><span class="sxs-lookup"><span data-stu-id="17a44-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="17a44-124">ATTACH_BY_REF_ONLY</span><span class="sxs-lookup"><span data-stu-id="17a44-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="17a44-125">Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, идентифицирующий вложение.</span><span class="sxs-lookup"><span data-stu-id="17a44-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="17a44-126">ATTACH_EMBEDDED_MSG</span><span class="sxs-lookup"><span data-stu-id="17a44-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="17a44-127">Свойство **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) содержит внедренный объект, который поддерживает интерфейс **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="17a44-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="17a44-128">ATTACH_OLE</span><span class="sxs-lookup"><span data-stu-id="17a44-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="17a44-129">Вложение представляет внедренный объект OLE.</span><span class="sxs-lookup"><span data-stu-id="17a44-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="17a44-130">ATTACH_BY_WEBREFERENCE</span><span class="sxs-lookup"><span data-stu-id="17a44-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="17a44-131">Содержимое вложения не в сообщении.</span><span class="sxs-lookup"><span data-stu-id="17a44-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="17a44-132">При создании, вложения у каждого объекта есть начальное значение **PR_ATTACH_METHOD** **NO_ATTACHMENT**.</span><span class="sxs-lookup"><span data-stu-id="17a44-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="17a44-133">Клиентские приложения и поставщиков услуг только необходимых для поддержки метод вложения, представленный значением **ATTACH_BY_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="17a44-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="17a44-134">Другие методы вложения являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="17a44-134">The other attachment methods are optional.</span></span> <span data-ttu-id="17a44-135">Хранилище сообщений не требует принудительного согласованность значение **PR_ATTACH_METHOD** и значения свойства вложения.</span><span class="sxs-lookup"><span data-stu-id="17a44-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="17a44-136">Для полные пути, которые можно использовать с **ATTACH_BY_REFERENCE** и **ATTACH_BY_REF_ONLY**рекомендуются универсальных имен именования соглашение (UNC).</span><span class="sxs-lookup"><span data-stu-id="17a44-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="17a44-137">С помощью **ATTACH_BY_REF_RESOLVE**абсолютный путь быстрее, так как диспетчер очереди MAPI преобразует вложения в **ATTACH_BY_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="17a44-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="17a44-138">Если значение **ATTACH_BY_REFERENCE** , **PR_ATTACH_DATA_BIN** должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="17a44-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="17a44-139">Исходящие шлюза можно преобразовать **ATTACH_BY_REFERENCE** вложения в **ATTACH_BY_VALUE** вложения, скопировав данные вложения в свойстве **PR_ATTACH_DATA_BIN** .</span><span class="sxs-lookup"><span data-stu-id="17a44-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="17a44-140">Если значение **ATTACH_BY_REF_RESOLVE** , **PR_ATTACH_DATA_BIN** должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="17a44-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="17a44-141">При отправке сообщения с вложением **ATTACH_BY_REF_RESOLVE** диспетчер очереди MAPI копирует данные вложения в **ATTACH_BY_VALUE** вложения.</span><span class="sxs-lookup"><span data-stu-id="17a44-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="17a44-142">Этот процесс разрешения помещает данные вложения в **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="17a44-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="17a44-143">Если значение **ATTACH_BY_REF_ONLY** , **PR_ATTACH_DATA_BIN** должна быть пустой и системы обмена сообщениями никогда не разрешает ссылку вложения.</span><span class="sxs-lookup"><span data-stu-id="17a44-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="17a44-144">Это значение используется, когда требуется отправить ссылку, но не данные.</span><span class="sxs-lookup"><span data-stu-id="17a44-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="17a44-145">Если объект OLE в формате OLE 2.0 **IStorage** , данных доступен через **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="17a44-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="17a44-146">Если объект OLE в формате OLE 1.0 **OLESTREAM** , данных доступен через **PR_ATTACH_DATA_BIN** как интерфейс **IStream**.</span><span class="sxs-lookup"><span data-stu-id="17a44-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="17a44-147">Можно определить тип кодировки OLE по значению **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="17a44-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="17a44-148">Дополнительные сведения о интерфейсов OLE и форматы *OLE Справочник программиста* см.</span><span class="sxs-lookup"><span data-stu-id="17a44-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="17a44-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="17a44-149">Remarks</span></span>

<span data-ttu-id="17a44-150">При **ATTACH_BY_WEBREFERENCE** **PR_ATTACH_METHOD** не является содержимое вложения в сообщении.</span><span class="sxs-lookup"><span data-stu-id="17a44-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="17a44-151">Вместо этого свойство **PR_ATTACH_LONG_FILENAME** содержит абсолютный URL-адрес для содержимого вложения, которая хранится в Интернете.</span><span class="sxs-lookup"><span data-stu-id="17a44-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="17a44-152">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="17a44-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17a44-153">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="17a44-153">Protocol specifications</span></span>

<span data-ttu-id="17a44-154">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17a44-154">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17a44-155">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="17a44-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17a44-156">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="17a44-156">Header files</span></span>

<span data-ttu-id="17a44-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17a44-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="17a44-158">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="17a44-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="17a44-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17a44-159">Mapitags.h</span></span>
  
> <span data-ttu-id="17a44-160">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="17a44-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17a44-161">См. также</span><span class="sxs-lookup"><span data-stu-id="17a44-161">See also</span></span>



[<span data-ttu-id="17a44-162">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="17a44-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="17a44-163">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="17a44-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17a44-164">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="17a44-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17a44-165">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="17a44-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17a44-166">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="17a44-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

