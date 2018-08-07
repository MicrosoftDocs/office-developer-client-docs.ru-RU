---
title: Каноническое свойство PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cdeb432e20f2779bbb625566108551748b48a01f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810857"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="23820-103">Каноническое свойство PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="23820-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="23820-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23820-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23820-105">Содержит идентификатор объекта ASN.1, который задает кодирование для вложения.</span><span class="sxs-lookup"><span data-stu-id="23820-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23820-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="23820-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23820-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="23820-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="23820-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="23820-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23820-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="23820-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="23820-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="23820-110">Data type:</span></span>  <br/> |<span data-ttu-id="23820-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="23820-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="23820-112">Область:</span><span class="sxs-lookup"><span data-stu-id="23820-112">Area:</span></span>  <br/> |<span data-ttu-id="23820-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="23820-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23820-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="23820-114">Remarks</span></span>

<span data-ttu-id="23820-115">Это свойство определяет алгоритм, используемый для преобразования данных в вложения.</span><span class="sxs-lookup"><span data-stu-id="23820-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="23820-116">**Примечание** Не следует путать **PR_ATTACH_ENCODING** и свойства **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="23820-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="23820-117">Они не пару и связанные с.</span><span class="sxs-lookup"><span data-stu-id="23820-117">They are not paired or related.</span></span> <span data-ttu-id="23820-118">**PR_ATTACH_TAG** — определяет приложения, изначально создавшего вложение.</span><span class="sxs-lookup"><span data-stu-id="23820-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="23820-119">«Объект» имеет гораздо более общие значение в идентификатор объекта терминов и в X.400, чем в объектно ориентированного программирования.</span><span class="sxs-lookup"><span data-stu-id="23820-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="23820-120">Идентификаторы объектов синтаксис и образец идентификатор объекта определены в MAPIOID. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="23820-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="23820-121">Значения для **PR_ATTACH_ENCODING** не только, определенных в MAPIOID. З.</span><span class="sxs-lookup"><span data-stu-id="23820-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="23820-122">Например вложенные файлы Macintosh можно использовать идентификатор, такие как файлы.</span><span class="sxs-lookup"><span data-stu-id="23820-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="23820-123">Полные сведения о идентификаторы объектов обратитесь к документации по ASN.1, X.208 и X.209.</span><span class="sxs-lookup"><span data-stu-id="23820-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="23820-124">Идентификатор объекта находится в элементе ссылка приложения среды FTBP (файл перенос текста часть).</span><span class="sxs-lookup"><span data-stu-id="23820-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23820-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="23820-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23820-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="23820-126">Protocol specifications</span></span>

<span data-ttu-id="23820-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23820-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23820-128">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="23820-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23820-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="23820-129">Header files</span></span>

<span data-ttu-id="23820-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23820-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="23820-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="23820-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="23820-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23820-132">Mapitags.h</span></span>
  
> <span data-ttu-id="23820-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="23820-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23820-134">См. также</span><span class="sxs-lookup"><span data-stu-id="23820-134">See also</span></span>



[<span data-ttu-id="23820-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="23820-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23820-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="23820-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23820-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="23820-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23820-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="23820-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

