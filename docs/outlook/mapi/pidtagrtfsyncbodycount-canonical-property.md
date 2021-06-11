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
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="6a60c-103">Каноническое свойство PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="6a60c-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="6a60c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a60c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a60c-105">Содержит количество важных символов текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a60c-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a60c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6a60c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a60c-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="6a60c-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="6a60c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6a60c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a60c-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="6a60c-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="6a60c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6a60c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a60c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6a60c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6a60c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6a60c-112">Area:</span></span>  <br/> |<span data-ttu-id="6a60c-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="6a60c-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a60c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a60c-114">Remarks</span></span>

<span data-ttu-id="6a60c-115">Функция [RTFSync](rtfsync.md) вычисляет количество символов в тексте, используя только те, которые считаются значимыми для сообщения.</span><span class="sxs-lookup"><span data-stu-id="6a60c-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="6a60c-116">Например, некоторое белое пространство и другие игнорируемые символы не учитываются в графе.</span><span class="sxs-lookup"><span data-stu-id="6a60c-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="6a60c-117">Это свойство является вспомогательным свойством Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="6a60c-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="6a60c-118">Эти свойства используются функцией **RTFSync** и не предназначены для непосредственного использования клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="6a60c-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6a60c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6a60c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a60c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6a60c-120">Protocol specifications</span></span>

<span data-ttu-id="6a60c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a60c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a60c-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6a60c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a60c-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a60c-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a60c-124">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="6a60c-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a60c-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6a60c-125">Header files</span></span>

<span data-ttu-id="6a60c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a60c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a60c-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6a60c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a60c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6a60c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6a60c-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6a60c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a60c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6a60c-130">See also</span></span>



[<span data-ttu-id="6a60c-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a60c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a60c-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a60c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a60c-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6a60c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a60c-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6a60c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

