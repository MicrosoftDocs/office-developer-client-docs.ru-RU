---
title: Каноническое свойство PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d2926b09dd3dfd89ab771206e0c8848415238eba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585481"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="a60af-103">Каноническое свойство PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="a60af-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="a60af-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a60af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a60af-105">Содержит объект вложения, обычно доступе через интерфейс объекта связывания и внедрения (OLE) **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="a60af-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a60af-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a60af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a60af-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="a60af-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="a60af-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a60af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a60af-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="a60af-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="a60af-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a60af-110">Data type:</span></span>  <br/> |<span data-ttu-id="a60af-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a60af-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a60af-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a60af-112">Area:</span></span>  <br/> |<span data-ttu-id="a60af-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="a60af-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a60af-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a60af-114">Remarks</span></span>

<span data-ttu-id="a60af-115">Это свойство содержит вложения, когда значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) **ATTACH_EMBEDDED_MSG** или **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="a60af-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="a60af-116">Можно определить тип кодировки OLE из **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60af-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="a60af-117">Для вложения, связанные со значением **ATTACH_EMBEDDED_MSG** интерфейс [IMessage:IMAPIProp](imessageimapiprop.md) можно использовать для более быстрого доступа.</span><span class="sxs-lookup"><span data-stu-id="a60af-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="a60af-118">Свойство **PR_ATTACH_DATA_OBJ** содержит собственные данные для отображения динамических внедренный объект OLE, и свойство **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) должны быть пустой или несуществующий.</span><span class="sxs-lookup"><span data-stu-id="a60af-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="a60af-119">Для вложения файла документа OLE поставщика хранилища сообщений, необходимо ответить на звонок [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на **PR_ATTACH_DATA_OBJ** и при необходимости может ответить на звонок на **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="a60af-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="a60af-120">Свойства **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** совместно использовать один и тот же идентификатор свойства и таким образом, два представления одного свойства.</span><span class="sxs-lookup"><span data-stu-id="a60af-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="a60af-121">Для объекта хранилища такие как составной файл в формате документа OLE 2.0, некоторых поставщиков услуг позволяет открыть с помощью интерфейса MAPI **IStreamDocfile** подкласс **IStream** без дополнительных членов, предназначено для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="a60af-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="a60af-122">Потенциальные сохранением является достаточно попыткой открыть **PR_ATTACH_DATA_OBJ** через **IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="a60af-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="a60af-123">Если возвращаются **MAPI_E_INTERFACE_NOT_SUPPORTED** клиента можно открыть **PR_ATTACH_DATA_BIN** с **IStream**.</span><span class="sxs-lookup"><span data-stu-id="a60af-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="a60af-124">Если клиентское приложение или поставщик услуг не могут открыть вложенные объекты вложения с помощью **PR_ATTACH_DATA_OBJ** с помощью **PR_ATTACH_METHOD**, следует использовать **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="a60af-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="a60af-125">Дополнительные сведения о интерфейсов OLE и форматов видеть [OLE и передачи данных](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="a60af-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a60af-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a60af-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a60af-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a60af-127">Protocol specifications</span></span>

<span data-ttu-id="a60af-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a60af-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a60af-129">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="a60af-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="a60af-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a60af-130">Header Files</span></span>

<span data-ttu-id="a60af-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a60af-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="a60af-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a60af-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="a60af-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a60af-133">Mapitags.h</span></span>
  
> <span data-ttu-id="a60af-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a60af-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a60af-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a60af-135">See also</span></span>



[<span data-ttu-id="a60af-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a60af-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a60af-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a60af-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a60af-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a60af-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a60af-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a60af-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

