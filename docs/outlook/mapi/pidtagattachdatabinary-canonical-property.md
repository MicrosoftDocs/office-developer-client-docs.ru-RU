---
title: Каноническое свойство PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356548"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="9cfda-103">Каноническое свойство PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="9cfda-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="9cfda-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cfda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cfda-105">Содержит двоичные данные вложения, обычно доступные с помощью интерфейса **IStream,** связывающих объекты и встраив их.</span><span class="sxs-lookup"><span data-stu-id="9cfda-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cfda-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9cfda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cfda-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="9cfda-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="9cfda-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9cfda-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cfda-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="9cfda-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="9cfda-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9cfda-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cfda-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9cfda-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9cfda-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9cfda-112">Area:</span></span>  <br/> |<span data-ttu-id="9cfda-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="9cfda-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cfda-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9cfda-114">Remarks</span></span>

<span data-ttu-id="9cfda-115">Это свойство содержит вложение, когда значение **свойства PR_ATTACH_METHOD** [(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)ATTACH_BY_VALUE, которое является обычным методом вложения и единственным, которое необходимо поддерживать.</span><span class="sxs-lookup"><span data-stu-id="9cfda-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="9cfda-116">**PR_ATTACH_DATA_BIN** также содержит вложение OLE 1.0 **OLESTREAM,** если значение PR_ATTACH_METHOD ATTACH_OLE. </span><span class="sxs-lookup"><span data-stu-id="9cfda-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="9cfda-117">**Вложения OLESTREAM** можно скопировать в файл, позвонив по методу OLE **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="9cfda-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="9cfda-118">Тип кодировки OLE можно определить из **свойства PR_ATTACH_TAG** [(PidTagAttachTag).](pidtagattachtag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9cfda-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="9cfda-119">Для вложения в файл OLE поставщик хранения сообщений должен отвечать на вызов [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **по PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)и может необязательно отвечать на **вызов PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="9cfda-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="9cfda-120">Обратите **внимание, PR_ATTACH_DATA_BIN** **и PR_ATTACH_DATA_OBJ** имеют один и тот же идентификатор свойств и таким образом являются двумя renditions одного и того же свойства.</span><span class="sxs-lookup"><span data-stu-id="9cfda-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="9cfda-121">Для объекта хранения, например сложного файла в формате docfile OLE 2.0, некоторые поставщики услуг позволяют открывать его с интерфейсом **MAPI IStreamDocfile** для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="9cfda-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="9cfda-122">Поставщик, который поддерживает **IStreamDocfile,**  должен PR_ATTACH_DATA_OBJ его на PR_ATTACH_DATA_BIN **.**</span><span class="sxs-lookup"><span data-stu-id="9cfda-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="9cfda-123">Дополнительные сведения об интерфейсах и форматах OLE см. в [OLE и Data Transfer.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cfda-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9cfda-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9cfda-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cfda-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9cfda-125">Protocol specifications</span></span>

<span data-ttu-id="9cfda-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cfda-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cfda-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="9cfda-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="9cfda-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="9cfda-128">Header Files</span></span>

<span data-ttu-id="9cfda-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cfda-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cfda-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9cfda-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="9cfda-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9cfda-131">Mapitags.h</span></span>
  
> <span data-ttu-id="9cfda-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9cfda-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cfda-133">См. также</span><span class="sxs-lookup"><span data-stu-id="9cfda-133">See also</span></span>



[<span data-ttu-id="9cfda-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9cfda-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cfda-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9cfda-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cfda-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9cfda-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cfda-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="9cfda-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

