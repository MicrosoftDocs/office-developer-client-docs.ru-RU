---
title: Каноническое свойство PidTagRtfSyncTrailingCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7efa8dccf4c2c6da0ad60688d06d241d336e3943
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581008"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="5db2d-103">Каноническое свойство PidTagRtfSyncTrailingCount</span><span class="sxs-lookup"><span data-stu-id="5db2d-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="5db2d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5db2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5db2d-105">Содержит число допускающие игнорирование символы, отображаемые после значительные символов сообщения.</span><span class="sxs-lookup"><span data-stu-id="5db2d-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5db2d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5db2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5db2d-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="5db2d-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="5db2d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5db2d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5db2d-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="5db2d-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="5db2d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5db2d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5db2d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5db2d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5db2d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5db2d-112">Area:</span></span>  <br/> |<span data-ttu-id="5db2d-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="5db2d-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5db2d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5db2d-114">Remarks</span></span>

<span data-ttu-id="5db2d-115">Это свойство является свойством дополнительный формат форматированный текст (RFT).</span><span class="sxs-lookup"><span data-stu-id="5db2d-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="5db2d-116">Эти свойства, используемые функцией [RTFSync](rtfsync.md) и не предназначен для непосредственного использования в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="5db2d-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5db2d-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5db2d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5db2d-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5db2d-118">Protocol specifications</span></span>

<span data-ttu-id="5db2d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5db2d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5db2d-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5db2d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5db2d-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5db2d-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5db2d-122">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="5db2d-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5db2d-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5db2d-123">Header files</span></span>

<span data-ttu-id="5db2d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5db2d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5db2d-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5db2d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5db2d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5db2d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5db2d-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5db2d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5db2d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5db2d-128">See also</span></span>



[<span data-ttu-id="5db2d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5db2d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5db2d-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5db2d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5db2d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5db2d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5db2d-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5db2d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

