---
title: Каноническое свойство PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339258"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="b843c-103">Каноническое свойство PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="b843c-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="b843c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b843c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b843c-105">Содержит полную тему сообщения.</span><span class="sxs-lookup"><span data-stu-id="b843c-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b843c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b843c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b843c-107">PR_SUBJECT, PR_SUBJECT_A PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="b843c-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="b843c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b843c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b843c-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="b843c-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="b843c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b843c-110">Data type:</span></span>  <br/> |<span data-ttu-id="b843c-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b843c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b843c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b843c-112">Area:</span></span>  <br/> |<span data-ttu-id="b843c-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="b843c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b843c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b843c-114">Remarks</span></span>

<span data-ttu-id="b843c-115">Эти свойства рекомендуются для всех объектов Message.</span><span class="sxs-lookup"><span data-stu-id="b843c-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="b843c-116">Эти свойства всегда являются полным текстом темы, то есть объединением префикса и нормализованной темы.</span><span class="sxs-lookup"><span data-stu-id="b843c-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="b843c-117">Если префикс отсутствует, нормализованная тема должна совпадать с темой.</span><span class="sxs-lookup"><span data-stu-id="b843c-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="b843c-118">Хранилище сообщений или поставщик транспорта использует как эти свойства, так и свойства **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) для вычисления нормализованной темы с использованием правила, описанного в разделе **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b843c-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="b843c-119">В свойствах subject обычно используются небольшие строки менее 256 символов, а поставщик хранилища сообщений не обязан поддерживать интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b843c-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="b843c-120">Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** , а затем последовательно прибегнуть к **IStream** , только если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="b843c-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="b843c-121">Для отчета это свойство содержит тему исходного сообщения, которая предшествует строке, указывающей на то, что произошло с сообщением.</span><span class="sxs-lookup"><span data-stu-id="b843c-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b843c-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b843c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b843c-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b843c-123">Protocol specifications</span></span>

<span data-ttu-id="b843c-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b843c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b843c-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b843c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b843c-126">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b843c-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b843c-127">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="b843c-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b843c-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b843c-128">Header files</span></span>

<span data-ttu-id="b843c-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b843c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="b843c-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b843c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="b843c-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b843c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="b843c-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b843c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b843c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b843c-133">See also</span></span>



[<span data-ttu-id="b843c-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b843c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b843c-135">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b843c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b843c-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b843c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b843c-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b843c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

