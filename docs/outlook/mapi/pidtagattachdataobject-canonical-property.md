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
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="4f38a-103">Каноническое свойство PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="4f38a-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="4f38a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f38a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f38a-105">Содержит объект вложения, доступ к которому обычно осуществляется с помощью интерфейса OLE **IStorage** для связывания и внедрения объектов.</span><span class="sxs-lookup"><span data-stu-id="4f38a-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f38a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4f38a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f38a-107">ПР_АТТАЧ_ДАТА_ОБЖ</span><span class="sxs-lookup"><span data-stu-id="4f38a-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="4f38a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4f38a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f38a-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="4f38a-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="4f38a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4f38a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f38a-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="4f38a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="4f38a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4f38a-112">Area:</span></span>  <br/> |<span data-ttu-id="4f38a-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="4f38a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f38a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f38a-114">Remarks</span></span>

<span data-ttu-id="4f38a-115">Это свойство содержит вложение, когда значение свойства **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) равно **аттач_ембеддед_мсг** или **аттач_оле**.</span><span class="sxs-lookup"><span data-stu-id="4f38a-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="4f38a-116">Тип кодирования OLE можно определить из **пр_аттач_таг** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4f38a-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="4f38a-117">Для вложений, связанных со значением **аттач_ембеддед_мсг** , можно использовать интерфейс [iMessage: IMAPIProp](imessageimapiprop.md) для более быстрого доступа.</span><span class="sxs-lookup"><span data-stu-id="4f38a-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="4f38a-118">Для внедренного динамического объекта OLE свойство **пр_аттач_дата_обж** содержит собственные сведения о отрисовке, а свойство **пр_аттач_рендеринг** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) должно быть либо несуществующим, либо пустым.</span><span class="sxs-lookup"><span data-stu-id="4f38a-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="4f38a-119">Для вложенного файла документа OLE поставщик хранилища сообщений должен отвечать на вызов [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) на **пр_аттач_дата_обж** , а также может ответить на вызов в **пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="4f38a-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="4f38a-120">Свойства **пр_аттач_дата_бин** и **пр_аттач_дата_обж** используют один и тот же идентификатор свойства, поэтому они являются двумя представлениями одного и того же свойства.</span><span class="sxs-lookup"><span data-stu-id="4f38a-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="4f38a-121">Для объекта хранилища, такого как составной файл в формате OLE 2,0 докфиле, некоторые поставщики услуг позволяют открыть его с помощью интерфейса MAPI **помощью istreamdocfile** , который является подКлассом **IStream** без дополнительных членов, предназначенный для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="4f38a-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="4f38a-122">Для того, чтобы выровнять попытки открыть **пр_аттач_дата_обж** через **помощью istreamdocfile**, достаточно сэкономить.</span><span class="sxs-lookup"><span data-stu-id="4f38a-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="4f38a-123">Если возвращается **мапи_е_интерфаце_нот_суппортед** , клиент может открыть **Пр_аттач_дата_бин** с помощью **IStream**.</span><span class="sxs-lookup"><span data-stu-id="4f38a-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="4f38a-124">Если клиентское приложение или поставщик услуг не может открыть вложенный объект с помощью **пр_аттач_дата_обж** с помощью **пр_аттач_месод**, он должен использовать **пр_аттач_дата_бин**.</span><span class="sxs-lookup"><span data-stu-id="4f38a-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="4f38a-125">Дополнительные сведения о OLE interfaces и formats можно найти в статье [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f38a-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f38a-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f38a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f38a-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4f38a-127">Protocol specifications</span></span>

<span data-ttu-id="4f38a-128">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f38a-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f38a-129">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4f38a-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="4f38a-130">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="4f38a-130">Header Files</span></span>

<span data-ttu-id="4f38a-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4f38a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f38a-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4f38a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f38a-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4f38a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="4f38a-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4f38a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f38a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="4f38a-135">See also</span></span>



[<span data-ttu-id="4f38a-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4f38a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f38a-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4f38a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f38a-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4f38a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f38a-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4f38a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

