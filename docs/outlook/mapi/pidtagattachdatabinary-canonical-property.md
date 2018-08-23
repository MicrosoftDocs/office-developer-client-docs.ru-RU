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
ms.openlocfilehash: 629746cedf8c6f4a8c960912a9ab1bcdc7a09e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574148"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="16487-103">Каноническое свойство PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="16487-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="16487-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16487-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16487-105">Содержит двоичные вложения данные обычно через интерфейс объекта связывания и внедрения (OLE) **IStream** .</span><span class="sxs-lookup"><span data-stu-id="16487-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16487-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="16487-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16487-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="16487-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="16487-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="16487-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16487-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="16487-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="16487-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="16487-110">Data type:</span></span>  <br/> |<span data-ttu-id="16487-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="16487-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="16487-112">Область:</span><span class="sxs-lookup"><span data-stu-id="16487-112">Area:</span></span>  <br/> |<span data-ttu-id="16487-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="16487-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16487-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="16487-114">Remarks</span></span>

<span data-ttu-id="16487-115">Это свойство содержит вложения, если значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) ATTACH_BY_VALUE, метод обычного вложения, и только один, которые должны поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="16487-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="16487-116">Если значение **PR_ATTACH_METHOD** ATTACH_OLE **PR_ATTACH_DATA_BIN** также содержит вложения OLE 1.0 **OLESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="16487-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="16487-117">**OLESTREAM** вложения могут быть скопированы в файл путем вызова метода OLE **IStream::CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="16487-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="16487-118">Тип кодировки OLE можно определить по свойству **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="16487-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="16487-119">Для вложения файла документа OLE поставщика хранилища сообщений, необходимо ответить на звонок [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) и при необходимости может ответить на звонок на **PR_ATTACH_DATA_BIN **.</span><span class="sxs-lookup"><span data-stu-id="16487-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="16487-120">Обратите внимание, что **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** совместно использовать один и тот же идентификатор свойства и таким образом, два представления одного свойства.</span><span class="sxs-lookup"><span data-stu-id="16487-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="16487-121">Для объекта хранилища например составные файл в формате документа OLE 2.0, некоторых поставщиков услуг позволяет открыть с помощью интерфейса MAPI **IStreamDocfile** для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="16487-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="16487-122">Поставщик, который поддерживает **IStreamDocfile** должен предоставлять на **PR_ATTACH_DATA_OBJ** и может при необходимости привести на **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="16487-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="16487-123">Дополнительные сведения о интерфейсов OLE и форматов видеть [OLE и передачи данных](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="16487-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="16487-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16487-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16487-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="16487-125">Protocol specifications</span></span>

<span data-ttu-id="16487-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16487-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16487-127">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="16487-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="16487-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="16487-128">Header Files</span></span>

<span data-ttu-id="16487-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16487-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="16487-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="16487-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="16487-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="16487-131">Mapitags.h</span></span>
  
> <span data-ttu-id="16487-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="16487-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16487-133">См. также</span><span class="sxs-lookup"><span data-stu-id="16487-133">See also</span></span>



[<span data-ttu-id="16487-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16487-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16487-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16487-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16487-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="16487-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16487-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="16487-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

