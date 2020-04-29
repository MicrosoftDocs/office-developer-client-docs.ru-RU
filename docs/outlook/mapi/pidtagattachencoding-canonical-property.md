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
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345495"
---
# <a name="pidtagattachencoding-canonical-property"></a><span data-ttu-id="921fc-103">Каноническое свойство PidTagAttachEncoding</span><span class="sxs-lookup"><span data-stu-id="921fc-103">PidTagAttachEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="921fc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="921fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="921fc-105">Содержит идентификатор объекта ASN. 1, указывающий кодировку для вложения.</span><span class="sxs-lookup"><span data-stu-id="921fc-105">Contains an ASN.1 object identifier that specifies the encoding for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="921fc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="921fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="921fc-107">PR_ATTACH_ENCODING</span><span class="sxs-lookup"><span data-stu-id="921fc-107">PR_ATTACH_ENCODING</span></span>  <br/> |
|<span data-ttu-id="921fc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="921fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="921fc-109">0x3702</span><span class="sxs-lookup"><span data-stu-id="921fc-109">0x3702</span></span>  <br/> |
|<span data-ttu-id="921fc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="921fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="921fc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="921fc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="921fc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="921fc-112">Area:</span></span>  <br/> |<span data-ttu-id="921fc-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="921fc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="921fc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="921fc-114">Remarks</span></span>

<span data-ttu-id="921fc-115">Это свойство определяет алгоритм, используемый для преобразования данных во вложении.</span><span class="sxs-lookup"><span data-stu-id="921fc-115">This property identifies the algorithm used to transform the data in an attachment.</span></span>
  
 <span data-ttu-id="921fc-116">**Note (Примечание** ) Свойства **PR_ATTACH_ENCODING** и **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) не следует путать.</span><span class="sxs-lookup"><span data-stu-id="921fc-116">**Note** The **PR_ATTACH_ENCODING** and **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) properties should not be confused.</span></span> <span data-ttu-id="921fc-117">Они не являются связанными или связанными.</span><span class="sxs-lookup"><span data-stu-id="921fc-117">They are not paired or related.</span></span> <span data-ttu-id="921fc-118">**PR_ATTACH_TAG** определяет приложение, которое изначально создало вложение.</span><span class="sxs-lookup"><span data-stu-id="921fc-118">**PR_ATTACH_TAG** identifies the application that originally generated the attachment.</span></span> <span data-ttu-id="921fc-119">"Объект" имеет гораздо больше общего смысла в идентификаторе объекта Term и в X. 400, чем в объектно ориентированном программировании.</span><span class="sxs-lookup"><span data-stu-id="921fc-119">"Object" has a much more general meaning in the term object identifier, and in X.400, than in object-oriented programming.</span></span> 
  
<span data-ttu-id="921fc-120">Синтаксис идентификатора объекта и примеры идентификаторов объектов определяются в МАПИОИД. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="921fc-120">The object identifier syntax and sample object identifiers are defined in the MAPIOID.H header file.</span></span> <span data-ttu-id="921fc-121">Значения **PR_ATTACH_ENCODING** не ограничиваются теми, что заданы в мапиоид. Высоты.</span><span class="sxs-lookup"><span data-stu-id="921fc-121">Values for **PR_ATTACH_ENCODING** are not limited to those defined in MAPIOID.H.</span></span> <span data-ttu-id="921fc-122">Например, прикрепленные файлы Macintosh могут использовать идентификатор, например Макбинари.</span><span class="sxs-lookup"><span data-stu-id="921fc-122">For example, attached Macintosh files can use an identifier such as MacBinary.</span></span> 
  
<span data-ttu-id="921fc-123">Для получения полных сведений об этих идентификаторах объектов, ознакомьтесь с документацией по ASN. 1, X. 208 и X. 209.</span><span class="sxs-lookup"><span data-stu-id="921fc-123">For complete information on these object identifiers, see the documentation on ASN.1, X.208, and X.209.</span></span> <span data-ttu-id="921fc-124">Идентификатор объекта находится в элементе ссылки на приложение в среде ФТБП (часть текста для передачи файлов).</span><span class="sxs-lookup"><span data-stu-id="921fc-124">The object identifier is found in the application-reference element of the FTBP (File Transfer Body Part) environment.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="921fc-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="921fc-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="921fc-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="921fc-126">Protocol specifications</span></span>

<span data-ttu-id="921fc-127">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="921fc-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="921fc-128">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="921fc-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="921fc-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="921fc-129">Header files</span></span>

<span data-ttu-id="921fc-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="921fc-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="921fc-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="921fc-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="921fc-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="921fc-132">Mapitags.h</span></span>
  
> <span data-ttu-id="921fc-133">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="921fc-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="921fc-134">См. также</span><span class="sxs-lookup"><span data-stu-id="921fc-134">See also</span></span>



[<span data-ttu-id="921fc-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="921fc-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="921fc-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="921fc-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="921fc-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="921fc-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="921fc-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="921fc-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

