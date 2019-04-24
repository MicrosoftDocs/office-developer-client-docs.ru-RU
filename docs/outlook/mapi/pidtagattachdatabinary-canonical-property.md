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
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="77c6b-103">Каноническое свойство PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="77c6b-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="77c6b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77c6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77c6b-105">Содержит двоичные данные вложения, доступ к которым осуществляется с помощью интерфейса OLE (технология \*\*\*\* связывания и внедрения объектов).</span><span class="sxs-lookup"><span data-stu-id="77c6b-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77c6b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="77c6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77c6b-107">ПР_АТТАЧ_ДАТА_БИН</span><span class="sxs-lookup"><span data-stu-id="77c6b-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="77c6b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="77c6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77c6b-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="77c6b-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="77c6b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="77c6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="77c6b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="77c6b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="77c6b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="77c6b-112">Area:</span></span>  <br/> |<span data-ttu-id="77c6b-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="77c6b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77c6b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="77c6b-114">Remarks</span></span>

<span data-ttu-id="77c6b-115">Это свойство содержит вложение, когда значение свойства **пр_аттач_месод** ([PIDTAGATTACHMETHOD](pidtagattachmethod-canonical-property.md)) равно аттач_би_валуе, которое является обычным методом вложения и только один, который требуется для поддержки.</span><span class="sxs-lookup"><span data-stu-id="77c6b-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="77c6b-116">**Пр_аттач_дата_бин** также содержит вложение OLE 1,0 **олестреам** , когда значение **пр_аттач_месод** равно аттач_оле.</span><span class="sxs-lookup"><span data-stu-id="77c6b-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="77c6b-117">Вложения **олестреам** можно скопировать в файл, вызвав метод OLE **IStream:: CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="77c6b-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="77c6b-118">Тип кодирования OLE можно определить в свойстве **пр_аттач_таг** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="77c6b-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="77c6b-119">Для вложенного файла документа OLE поставщик хранилища сообщений должен отвечать на вызов [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) на **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), а также может ответить на вызов в \*\*пр_аттач_дата_бин \*\*.</span><span class="sxs-lookup"><span data-stu-id="77c6b-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="77c6b-120">Обратите внимание, что **пр_аттач_дата_бин** и **пр_аттач_дата_обж** совместно используют один и тот же идентификатор свойства и, таким образом, являются двумя представлениями одного и того же свойства.</span><span class="sxs-lookup"><span data-stu-id="77c6b-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="77c6b-121">Для объекта хранилища, например составного файла в формате OLE 2,0 докфиле, некоторые поставщики услуг позволяют открыть его с помощью интерфейса MAPI **помощью istreamdocfile** для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="77c6b-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="77c6b-122">Поставщик, который поддерживает **помощью istreamdocfile** , должен предоставлять его в **пр_аттач_дата_обж** и может при необходимости предоставлять его в **пр_аттач_дата_бин**.</span><span class="sxs-lookup"><span data-stu-id="77c6b-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="77c6b-123">Дополнительные сведения о OLE interfaces и formats можно найти в статье [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="77c6b-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="77c6b-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77c6b-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77c6b-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="77c6b-125">Protocol specifications</span></span>

<span data-ttu-id="77c6b-126">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77c6b-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77c6b-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="77c6b-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="77c6b-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="77c6b-128">Header Files</span></span>

<span data-ttu-id="77c6b-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="77c6b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="77c6b-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="77c6b-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="77c6b-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="77c6b-131">Mapitags.h</span></span>
  
> <span data-ttu-id="77c6b-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="77c6b-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77c6b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="77c6b-133">See also</span></span>



[<span data-ttu-id="77c6b-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="77c6b-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77c6b-135">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="77c6b-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77c6b-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="77c6b-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77c6b-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="77c6b-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

