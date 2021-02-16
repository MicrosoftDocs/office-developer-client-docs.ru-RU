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
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="108aa-103">Каноническое свойство PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="108aa-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="108aa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="108aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="108aa-105">Содержит двоичные данные вложений, которые обычно доступны через интерфейс **IStream** для связывания и встраивления объектов (OLE).</span><span class="sxs-lookup"><span data-stu-id="108aa-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="108aa-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="108aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="108aa-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="108aa-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="108aa-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="108aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="108aa-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="108aa-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="108aa-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="108aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="108aa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="108aa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="108aa-112">Область:</span><span class="sxs-lookup"><span data-stu-id="108aa-112">Area:</span></span>  <br/> |<span data-ttu-id="108aa-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="108aa-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="108aa-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="108aa-114">Remarks</span></span>

<span data-ttu-id="108aa-115">Это свойство содержит вложение, если значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)ATTACH_BY_VALUE, который является обычным методом вложения и единственным, который требуется поддерживать.</span><span class="sxs-lookup"><span data-stu-id="108aa-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="108aa-116">**PR_ATTACH_DATA_BIN** также содержит вложение OLE 1.0 **OLESTREAM,** если PR_ATTACH_METHOD значение **ATTACH_OLE.**</span><span class="sxs-lookup"><span data-stu-id="108aa-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="108aa-117">**Вложения OLESTREAM** можно скопировать в файл, вызывая метод OLE **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="108aa-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="108aa-118">Тип кодиировки OLE можно определить из свойства **PR_ATTACH_TAG** ([PidTagAttachTag).](pidtagattachtag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="108aa-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="108aa-119">Для вложенного файла документа OLE поставщик хранения сообщений должен ответить на вызов [IMAPIProp::OpenProperty](imapiprop-openproperty.md) в **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)и при желании ответить на вызов PR_ATTACH_DATA_BIN **.**</span><span class="sxs-lookup"><span data-stu-id="108aa-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="108aa-120">Обратите **внимание PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** одно и то же идентификатор свойства и, следовательно, являются двумя его двумя.</span><span class="sxs-lookup"><span data-stu-id="108aa-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="108aa-121">Для объекта хранилища, например составного файла в формате docfile OLE 2.0, некоторые поставщики услуг позволяют открывать его с помощью интерфейса **MAPI IStreamDocfile** для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="108aa-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="108aa-122">Поставщик, который поддерживает **IStreamDocfile,**  должен показать его на PR_ATTACH_DATA_OBJ и при желании может выставить его **на PR_ATTACH_DATA_BIN.**</span><span class="sxs-lookup"><span data-stu-id="108aa-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="108aa-123">Дополнительные сведения об интерфейсах и форматах OLE см. в [OLE и передаче данных.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="108aa-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="108aa-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="108aa-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="108aa-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="108aa-125">Protocol specifications</span></span>

<span data-ttu-id="108aa-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="108aa-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="108aa-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="108aa-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="108aa-128">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="108aa-128">Header Files</span></span>

<span data-ttu-id="108aa-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="108aa-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="108aa-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="108aa-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="108aa-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="108aa-131">Mapitags.h</span></span>
  
> <span data-ttu-id="108aa-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="108aa-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="108aa-133">См. также</span><span class="sxs-lookup"><span data-stu-id="108aa-133">See also</span></span>



[<span data-ttu-id="108aa-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="108aa-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="108aa-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="108aa-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="108aa-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="108aa-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="108aa-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="108aa-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

