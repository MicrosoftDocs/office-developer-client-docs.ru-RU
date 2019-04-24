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
description: 'Дата последнего изменения: 07 сентября 2016 г.'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327260"
---
# <a name="pidtagattachmethod-canonical-property"></a><span data-ttu-id="9a96a-103">Каноническое свойство PidTagAttachMethod</span><span class="sxs-lookup"><span data-stu-id="9a96a-103">PidTagAttachMethod Canonical Property</span></span>

 
  
<span data-ttu-id="9a96a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a96a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a96a-105">Содержит константу, определенную MAPI, которая представляет способ доступа к содержимому вложения.</span><span class="sxs-lookup"><span data-stu-id="9a96a-105">Contains a MAPI-defined constant representing the way the contents of an attachment can be accessed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a96a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9a96a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a96a-107">ПР_АТТАЧ_МЕСОД</span><span class="sxs-lookup"><span data-stu-id="9a96a-107">PR_ATTACH_METHOD</span></span>  <br/> |
|<span data-ttu-id="9a96a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9a96a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a96a-109">0x3705</span><span class="sxs-lookup"><span data-stu-id="9a96a-109">0x3705</span></span>  <br/> |
|<span data-ttu-id="9a96a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9a96a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a96a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9a96a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9a96a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9a96a-112">Area:</span></span>  <br/> |<span data-ttu-id="9a96a-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="9a96a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a96a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a96a-114">Remarks</span></span>

<span data-ttu-id="9a96a-115">Это свойство может иметь только одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9a96a-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="9a96a-116">НО_АТТАЧМЕНТ</span><span class="sxs-lookup"><span data-stu-id="9a96a-116">NO_ATTACHMENT</span></span> 
  
> <span data-ttu-id="9a96a-117">Вложение только что было создано.</span><span class="sxs-lookup"><span data-stu-id="9a96a-117">The attachment has just been created.</span></span> 
    
<span data-ttu-id="9a96a-118">АТТАЧ_БИ_ВАЛУЕ</span><span class="sxs-lookup"><span data-stu-id="9a96a-118">ATTACH_BY_VALUE</span></span> 
  
> <span data-ttu-id="9a96a-119">Свойство **пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) содержит данные вложений.</span><span class="sxs-lookup"><span data-stu-id="9a96a-119">The **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property contains the attachment data.</span></span> 
    
<span data-ttu-id="9a96a-120">АТТАЧ_БИ_РЕФЕРЕНЦЕ</span><span class="sxs-lookup"><span data-stu-id="9a96a-120">ATTACH_BY_REFERENCE</span></span> 
  
> <span data-ttu-id="9a96a-121">Свойство **пр_аттач_паснаме** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) или **пр_аттач_лонг_паснаме** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) содержит полный путь, определяющий вложение получателям, у которых есть доступ к общему файлу. сервер.</span><span class="sxs-lookup"><span data-stu-id="9a96a-121">The **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) or **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) property contains a fully-qualified path identifying the attachment to recipients with access to a common file server.</span></span> 
    
<span data-ttu-id="9a96a-122">АТТАЧ_БИ_РЕФ_РЕСОЛВЕ</span><span class="sxs-lookup"><span data-stu-id="9a96a-122">ATTACH_BY_REF_RESOLVE</span></span> 
  
> <span data-ttu-id="9a96a-123">Свойство **пр_аттач_паснаме** или **пр_аттач_лонг_паснаме** содержит полный путь, указывающий вложение.</span><span class="sxs-lookup"><span data-stu-id="9a96a-123">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="9a96a-124">АТТАЧ_БИ_РЕФ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="9a96a-124">ATTACH_BY_REF_ONLY</span></span> 
  
> <span data-ttu-id="9a96a-125">Свойство **пр_аттач_паснаме** или **пр_аттач_лонг_паснаме** содержит полный путь, указывающий вложение.</span><span class="sxs-lookup"><span data-stu-id="9a96a-125">The **PR_ATTACH_PATHNAME** or **PR_ATTACH_LONG_PATHNAME** property contains a fully-qualified path identifying the attachment.</span></span> 
    
<span data-ttu-id="9a96a-126">АТТАЧ_ЕМБЕДДЕД_МСГ</span><span class="sxs-lookup"><span data-stu-id="9a96a-126">ATTACH_EMBEDDED_MSG</span></span> 
  
> <span data-ttu-id="9a96a-127">Свойство **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) содержит внедренный объект, который поддерживает интерфейс **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="9a96a-127">The **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property contains an embedded object that supports the **IMessage** interface.</span></span> 
    
<span data-ttu-id="9a96a-128">АТТАЧ_ОЛЕ</span><span class="sxs-lookup"><span data-stu-id="9a96a-128">ATTACH_OLE</span></span> 
  
> <span data-ttu-id="9a96a-129">Вложение является внедренным объектом OLE.</span><span class="sxs-lookup"><span data-stu-id="9a96a-129">The attachment is an embedded OLE object.</span></span>
    
<span data-ttu-id="9a96a-130">АТТАЧ_БИ_ВЕБРЕФЕРЕНЦЕ</span><span class="sxs-lookup"><span data-stu-id="9a96a-130">ATTACH_BY_WEBREFERENCE</span></span> 
  
> <span data-ttu-id="9a96a-131">Содержимое вложения отсутствует в сообщении.</span><span class="sxs-lookup"><span data-stu-id="9a96a-131">The attachment content is not in the message.</span></span> 
    
<span data-ttu-id="9a96a-132">При создании все объекты вложения имеют начальное значение **пр_аттач_месод** для **но_аттачмент**.</span><span class="sxs-lookup"><span data-stu-id="9a96a-132">When created, all attachment objects have an initial **PR_ATTACH_METHOD** value of **NO_ATTACHMENT**.</span></span> 
  
<span data-ttu-id="9a96a-133">Клиентские приложения и поставщики услуг необходимы только для поддержки метода вложения, представленного значением **аттач_би_валуе** .</span><span class="sxs-lookup"><span data-stu-id="9a96a-133">Client applications and service providers are only required to support the attachment method represented by the **ATTACH_BY_VALUE** value.</span></span> <span data-ttu-id="9a96a-134">Другие методы вложения являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="9a96a-134">The other attachment methods are optional.</span></span> <span data-ttu-id="9a96a-135">Хранилище сообщений не обеспечивает никакой согласованности между значением **пр_аттач_месод** и значениями других свойств вложения.</span><span class="sxs-lookup"><span data-stu-id="9a96a-135">The message store does not enforce any consistency between the value of **PR_ATTACH_METHOD** and the values of the other attachment properties.</span></span> 
  
<span data-ttu-id="9a96a-136">Имена в формате UNC рекомендуются для полных путей, которые следует использовать с **аттач_би_референце** и **аттач_би_реф_онли**.</span><span class="sxs-lookup"><span data-stu-id="9a96a-136">Universal naming convention (UNC) names are recommended for fully-qualified paths, which should be used with **ATTACH_BY_REFERENCE** and **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="9a96a-137">В **аттач_би_реф_ресолве**абсолютный путь выполняется быстрее, так как диспетчер очереди MAPI преобразует вложение в **аттач_би_валуе**.</span><span class="sxs-lookup"><span data-stu-id="9a96a-137">With **ATTACH_BY_REF_RESOLVE**, an absolute path is faster, because the MAPI spooler converts the attachment to **ATTACH_BY_VALUE**.</span></span> 
  
<span data-ttu-id="9a96a-138">Если задано значение **аттач_би_референце** , **пр_аттач_дата_бин** должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="9a96a-138">If **ATTACH_BY_REFERENCE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="9a96a-139">Исходящий шлюз может превратить вложение **аттач_би_референце** в вложение **аттач_би_валуе** путем копирования данных вложения в свойство **пр_аттач_дата_бин** .</span><span class="sxs-lookup"><span data-stu-id="9a96a-139">An outbound gateway can turn an **ATTACH_BY_REFERENCE** attachment into an **ATTACH_BY_VALUE** attachment by copying the attachment data into the **PR_ATTACH_DATA_BIN** property.</span></span> 
  
<span data-ttu-id="9a96a-140">Если задано значение **аттач_би_реф_ресолве** , **пр_аттач_дата_бин** должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="9a96a-140">If **ATTACH_BY_REF_RESOLVE** is set, **PR_ATTACH_DATA_BIN** must be empty.</span></span> <span data-ttu-id="9a96a-141">При отправке сообщения, содержащего вложение **аттач_би_реф_ресолве** , диспетчер очереди MAPI копирует данные вложения в вложение **аттач_би_валуе** .</span><span class="sxs-lookup"><span data-stu-id="9a96a-141">When the message that contains the **ATTACH_BY_REF_RESOLVE** attachment is sent, the MAPI spooler copies the attachment data into an **ATTACH_BY_VALUE** attachment.</span></span> <span data-ttu-id="9a96a-142">В этом процессе разрешения данные вложений размещаются в **пр_аттач_дата_бин**.</span><span class="sxs-lookup"><span data-stu-id="9a96a-142">This resolution process places the attachment data in **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="9a96a-143">Если задано значение **аттач_би_реф_онли** , **пр_аттач_дата_бин** должно быть пустым, а система обмена сообщениями никогда не разрешает ссылку вложения.</span><span class="sxs-lookup"><span data-stu-id="9a96a-143">If **ATTACH_BY_REF_ONLY** is set, **PR_ATTACH_DATA_BIN** must be empty, and the messaging system never resolves the attachment reference.</span></span> <span data-ttu-id="9a96a-144">Используйте это значение, если хотите отправить ссылку, но не данные.</span><span class="sxs-lookup"><span data-stu-id="9a96a-144">Use this value when you want to send the link but not the data.</span></span> 
  
<span data-ttu-id="9a96a-145">Если OLE-объект находится в формате **ISTORAGE** OLE 2,0, доступ к данным осуществляется с помощью **пр_аттач_дата_обж**.</span><span class="sxs-lookup"><span data-stu-id="9a96a-145">When the OLE object is in OLE 2.0 **IStorage** format, the data is accessible through **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="9a96a-146">Когда объект OLE представлен в формате OLE 1,0 **олестреам** , доступ к данным предоставляется через **Пр_аттач_дата_бин** в виде **IStream**.</span><span class="sxs-lookup"><span data-stu-id="9a96a-146">When the OLE object is in OLE 1.0 **OLESTREAM** format, the data is accessible through **PR_ATTACH_DATA_BIN** as an **IStream**.</span></span> <span data-ttu-id="9a96a-147">Тип OLE-кодировки можно определить с помощью значения **пр_аттач_таг** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9a96a-147">The type of the OLE encoding can be determined by the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) value.</span></span> 
  
<span data-ttu-id="9a96a-148">Дополнительные сведения о интерфейсах и форматах OLE приведены в *справочнике по OLE* для программистов.</span><span class="sxs-lookup"><span data-stu-id="9a96a-148">For more information on OLE interfaces and formats, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9a96a-149">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a96a-149">Remarks</span></span>

<span data-ttu-id="9a96a-150">Если для параметра **пр_аттач_месод** задано значение **аттач_би_вебреференце**, содержимое вложения отсутствует в сообщении.</span><span class="sxs-lookup"><span data-stu-id="9a96a-150">When the **PR_ATTACH_METHOD** is **ATTACH_BY_WEBREFERENCE**, the attachment content is not in the message.</span></span> <span data-ttu-id="9a96a-151">Вместо этого свойство **пр_аттач_лонг_филенаме** содержит абсолютный URL-адрес содержимого вложений, которое хранится в сети.</span><span class="sxs-lookup"><span data-stu-id="9a96a-151">Instead, the **PR_ATTACH_LONG_FILENAME** property contains an absolute URL to the attachment content, which is stored online.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9a96a-152">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9a96a-152">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a96a-153">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9a96a-153">Protocol specifications</span></span>

<span data-ttu-id="9a96a-154">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a96a-154">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a96a-155">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="9a96a-155">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a96a-156">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9a96a-156">Header files</span></span>

<span data-ttu-id="9a96a-157">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9a96a-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a96a-158">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9a96a-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a96a-159">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9a96a-159">Mapitags.h</span></span>
  
> <span data-ttu-id="9a96a-160">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="9a96a-160">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a96a-161">См. также</span><span class="sxs-lookup"><span data-stu-id="9a96a-161">See also</span></span>



[<span data-ttu-id="9a96a-162">Каноническое свойство PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="9a96a-162">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)


[<span data-ttu-id="9a96a-163">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9a96a-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a96a-164">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9a96a-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a96a-165">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9a96a-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a96a-166">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9a96a-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

