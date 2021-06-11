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
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339286"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="0d34b-103">Каноническое свойство PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="0d34b-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="0d34b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d34b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d34b-105">Содержит объект вложения, обычно доступный с помощью интерфейса **IStorage** , связывающий объект и встраив его.</span><span class="sxs-lookup"><span data-stu-id="0d34b-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d34b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0d34b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d34b-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="0d34b-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="0d34b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0d34b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d34b-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="0d34b-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="0d34b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0d34b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d34b-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="0d34b-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="0d34b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0d34b-112">Area:</span></span>  <br/> |<span data-ttu-id="0d34b-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="0d34b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d34b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d34b-114">Remarks</span></span>

<span data-ttu-id="0d34b-115">Это свойство содержит вложение, когда значение **свойства PR_ATTACH_METHOD**  [(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)ATTACH_EMBEDDED_MSG **или ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="0d34b-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="0d34b-116">Тип кодировки OLE можно определить по **PR_ATTACH_TAG** [(PidTagAttachTag).](pidtagattachtag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0d34b-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="0d34b-117">Для вложения, связанного **с ATTACH_EMBEDDED_MSG** значением, интерфейс [IMessage:IMAPIProp](imessageimapiprop.md) можно использовать для более быстрого доступа.</span><span class="sxs-lookup"><span data-stu-id="0d34b-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="0d34b-118">Для встроенного динамического объекта OLE свойство **PR_ATTACH_DATA_OBJ** содержит собственные данные отрисовки, а свойство **PR_ATTACH_RENDERING** [(PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)должно быть несущестным или пустым.</span><span class="sxs-lookup"><span data-stu-id="0d34b-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="0d34b-119">Для вложения в файл OLE поставщик хранения сообщений должен отвечать на вызов [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_ATTACH_DATA_OBJ** и может необязательным образом отвечать на вызов PR_ATTACH_DATA_BIN [(PidTagAttachDataBinary).](pidtagattachdatabinary-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="0d34b-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="0d34b-120">Свойства **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** имеют один и тот же идентификатор свойств и, таким образом, являются двумя renditions одного и того же свойства.</span><span class="sxs-lookup"><span data-stu-id="0d34b-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="0d34b-121">Для объекта хранения, например сложного файла в формате docfile OLE 2.0, некоторые поставщики услуг позволяют открывать его с интерфейсом MAPI **IStreamDocfile** , **подклассом IStream** без дополнительных членов, предназначенным для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="0d34b-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="0d34b-122">Возможной экономии достаточно, чтобы оправдать  попытку открыть PR_ATTACH_DATA_OBJ **через IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="0d34b-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="0d34b-123">Если **MAPI_E_INTERFACE_NOT_SUPPORTED** возвращается, клиент может открыть  PR_ATTACH_DATA_BIN **iStream**.</span><span class="sxs-lookup"><span data-stu-id="0d34b-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="0d34b-124">Если клиентская заявка или поставщик услуг не  могут открыть подобект вложения с помощью PR_ATTACH_DATA_OBJ с помощью **PR_ATTACH_METHOD,** он должен использовать **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="0d34b-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="0d34b-125">Дополнительные сведения об интерфейсах и форматах OLE см. в [OLE и Data Transfer.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d34b-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d34b-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0d34b-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d34b-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0d34b-127">Protocol specifications</span></span>

<span data-ttu-id="0d34b-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d34b-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d34b-129">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="0d34b-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="0d34b-130">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0d34b-130">Header Files</span></span>

<span data-ttu-id="0d34b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d34b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d34b-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0d34b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d34b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0d34b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0d34b-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0d34b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d34b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="0d34b-135">See also</span></span>



[<span data-ttu-id="0d34b-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d34b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d34b-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d34b-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d34b-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0d34b-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d34b-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0d34b-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

