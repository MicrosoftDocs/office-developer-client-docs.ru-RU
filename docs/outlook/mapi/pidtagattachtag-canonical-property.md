---
title: Каноническое свойство PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: af5d05ee6d3592694952002c16e16188c3e458a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565622"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="1e117-103">Каноническое свойство PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="1e117-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="1e117-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e117-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e117-105">Содержит идентификатор объекта ASN.1 определение приложения, предоставленные вложения.</span><span class="sxs-lookup"><span data-stu-id="1e117-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e117-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1e117-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e117-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="1e117-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="1e117-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1e117-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e117-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="1e117-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="1e117-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1e117-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e117-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e117-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e117-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1e117-112">Area:</span></span>  <br/> |<span data-ttu-id="1e117-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="1e117-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e117-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e117-114">Remarks</span></span>

<span data-ttu-id="1e117-115">Это свойство определяет приложения, изначально создавшего вложение.</span><span class="sxs-lookup"><span data-stu-id="1e117-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="1e117-116">**Примечание** Не следует путать свойства **PR_ATTACH_TAG** и **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1e117-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="1e117-117">Они не пару и связанные с.</span><span class="sxs-lookup"><span data-stu-id="1e117-117">They are not paired or related.</span></span> <span data-ttu-id="1e117-118">**PR_ATTACH_ENCODING** определяет алгоритм, используемый для преобразования данных в вложения.</span><span class="sxs-lookup"><span data-stu-id="1e117-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="1e117-119">«Объект» имеет значение намного более общие в идентификатор объекта терминов и об использовании X.400, чем в объектно ориентированного программирования.</span><span class="sxs-lookup"><span data-stu-id="1e117-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="1e117-120">Идентификаторы объектов синтаксис и образец идентификатор объекта определены в MAPIOID. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="1e117-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="1e117-121">Значения для **PR_ATTACH_TAG** не только, определенных в MAPIOID. З.</span><span class="sxs-lookup"><span data-stu-id="1e117-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="1e117-122">Полные сведения о идентификаторы объектов обратитесь к документации по ASN.1, X.208 и X.209.</span><span class="sxs-lookup"><span data-stu-id="1e117-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="1e117-123">Идентификатор объекта находится в элементе ссылка приложения среды часть перенос текста файла (FTBP).</span><span class="sxs-lookup"><span data-stu-id="1e117-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e117-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1e117-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e117-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1e117-125">Protocol specifications</span></span>

<span data-ttu-id="1e117-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e117-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e117-127">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="1e117-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e117-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1e117-128">Header files</span></span>

<span data-ttu-id="1e117-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e117-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e117-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1e117-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e117-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e117-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1e117-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1e117-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e117-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1e117-133">See also</span></span>



[<span data-ttu-id="1e117-134">Каноническое свойство PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="1e117-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="1e117-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1e117-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e117-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1e117-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e117-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1e117-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e117-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1e117-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

