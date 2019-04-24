---
title: Каноническое свойство PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331257"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="084c1-103">Каноническое свойство PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="084c1-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="084c1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="084c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="084c1-105">Содержит количество значащих символов текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="084c1-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="084c1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="084c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="084c1-107">ПР_РТФ_СИНК_БОДИ_КАУНТ</span><span class="sxs-lookup"><span data-stu-id="084c1-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="084c1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="084c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="084c1-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="084c1-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="084c1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="084c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="084c1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="084c1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="084c1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="084c1-112">Area:</span></span>  <br/> |<span data-ttu-id="084c1-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="084c1-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="084c1-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="084c1-114">Remarks</span></span>

<span data-ttu-id="084c1-115">Функция [ртфсинк](rtfsync.md) вычисляет количество символов в тексте, используя только те, которые считаются значащими для сообщения.</span><span class="sxs-lookup"><span data-stu-id="084c1-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="084c1-116">Например, некоторые пробелы и другие игнорируемые символы пропускаются из числа.</span><span class="sxs-lookup"><span data-stu-id="084c1-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="084c1-117">Это свойство является дополнительным свойством в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="084c1-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="084c1-118">Эти свойства используются функцией **ртфсинк** и не предназначены для непосредственного использования клиентскими приложениями.</span><span class="sxs-lookup"><span data-stu-id="084c1-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="084c1-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="084c1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="084c1-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="084c1-120">Protocol specifications</span></span>

<span data-ttu-id="084c1-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="084c1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="084c1-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="084c1-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="084c1-123">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="084c1-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="084c1-124">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="084c1-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="084c1-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="084c1-125">Header files</span></span>

<span data-ttu-id="084c1-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="084c1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="084c1-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="084c1-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="084c1-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="084c1-128">Mapitags.h</span></span>
  
> <span data-ttu-id="084c1-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="084c1-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="084c1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="084c1-130">See also</span></span>



[<span data-ttu-id="084c1-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="084c1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="084c1-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="084c1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="084c1-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="084c1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="084c1-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="084c1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

