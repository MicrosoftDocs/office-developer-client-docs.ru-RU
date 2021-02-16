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
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361084"
---
# <a name="pidtagattachtag-canonical-property"></a><span data-ttu-id="ad776-103">Каноническое свойство PidTagAttachTag</span><span class="sxs-lookup"><span data-stu-id="ad776-103">PidTagAttachTag Canonical Property</span></span>

  
  
<span data-ttu-id="ad776-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad776-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad776-105">Содержит идентификатор объекта ASN.1, определяющий приложение, которое предоставило вложение.</span><span class="sxs-lookup"><span data-stu-id="ad776-105">Contains an ASN.1 object identifier specifying the application that supplied an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad776-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ad776-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad776-107">PR_ATTACH_TAG</span><span class="sxs-lookup"><span data-stu-id="ad776-107">PR_ATTACH_TAG</span></span>  <br/> |
|<span data-ttu-id="ad776-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ad776-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad776-109">0x370A</span><span class="sxs-lookup"><span data-stu-id="ad776-109">0x370A</span></span>  <br/> |
|<span data-ttu-id="ad776-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ad776-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad776-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ad776-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ad776-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ad776-112">Area:</span></span>  <br/> |<span data-ttu-id="ad776-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="ad776-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad776-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad776-114">Remarks</span></span>

<span data-ttu-id="ad776-115">Это свойство определяет приложение, которое изначально вызвало вложение.</span><span class="sxs-lookup"><span data-stu-id="ad776-115">This property identifies the application that originally generated the attachment.</span></span>
  
 <span data-ttu-id="ad776-116">**Примечание** Свойства **PR_ATTACH_ENCODING** ([PidTagAttachEncoding)](pidtagattachencoding-canonical-property.md) **и** PR_ATTACH_TAG не следует путать.</span><span class="sxs-lookup"><span data-stu-id="ad776-116">**Note** The **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) and **PR_ATTACH_TAG** properties should not be confused.</span></span> <span data-ttu-id="ad776-117">Они не связаны и не связаны.</span><span class="sxs-lookup"><span data-stu-id="ad776-117">They are not paired or related.</span></span> <span data-ttu-id="ad776-118">**PR_ATTACH_ENCODING** определяет алгоритм, используемый для преобразования данных во вложении.</span><span class="sxs-lookup"><span data-stu-id="ad776-118">**PR_ATTACH_ENCODING** identifies the algorithm used to transform the data in an attachment.</span></span> <span data-ttu-id="ad776-119">"Object" имеет гораздо более общее значение в идентификаторе объекта термина и в использовании X.400, чем в объектно-ориентированном программировании.</span><span class="sxs-lookup"><span data-stu-id="ad776-119">"Object" has a much more general meaning in the term object identifier, and in X.400 usage, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="ad776-120">Синтаксис идентификатора объекта и образцы идентификаторов объектов определены в MAPIOID. Файл h-загона.</span><span class="sxs-lookup"><span data-stu-id="ad776-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="ad776-121">Значения **для** PR_ATTACH_TAG не ограничиваются значениями, определенными в MAPIOID.H.</span><span class="sxs-lookup"><span data-stu-id="ad776-121">Values for **PR_ATTACH_TAG** are not limited to those defined in MAPIOID.H.</span></span> 
  
<span data-ttu-id="ad776-122">Полные сведения об этих идентификаторах объектов см. в документации по ASN.1, X.208 и X.209.</span><span class="sxs-lookup"><span data-stu-id="ad776-122">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="ad776-123">Идентификатор объекта находится в элементе application-reference среды FTBP.</span><span class="sxs-lookup"><span data-stu-id="ad776-123">The object identifier is found in the application-reference element of the File Transfer Body Part (FTBP) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad776-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ad776-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad776-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ad776-125">Protocol specifications</span></span>

<span data-ttu-id="ad776-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad776-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad776-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="ad776-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad776-128">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="ad776-128">Header files</span></span>

<span data-ttu-id="ad776-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad776-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad776-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ad776-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad776-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad776-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ad776-132">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ad776-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad776-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ad776-133">See also</span></span>



[<span data-ttu-id="ad776-134">Каноническое свойство PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="ad776-134">PidTagAttachMimeTag Canonical Property</span></span>](pidtagattachmimetag-canonical-property.md)


[<span data-ttu-id="ad776-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ad776-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad776-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ad776-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad776-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ad776-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad776-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ad776-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

