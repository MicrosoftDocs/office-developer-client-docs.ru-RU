---
title: Каноническое свойство PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400973"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="06e67-103">Каноническое свойство PidTagRtfSyncBodyCrc</span><span class="sxs-lookup"><span data-stu-id="06e67-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="06e67-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06e67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06e67-105">Содержит флажок контрольная сумма (контрольной СУММЫ), вычисленные для текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="06e67-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06e67-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="06e67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06e67-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="06e67-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="06e67-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="06e67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06e67-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="06e67-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="06e67-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="06e67-110">Data type:</span></span>  <br/> |<span data-ttu-id="06e67-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06e67-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06e67-112">Область:</span><span class="sxs-lookup"><span data-stu-id="06e67-112">Area:</span></span>  <br/> |<span data-ttu-id="06e67-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="06e67-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06e67-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="06e67-114">Remarks</span></span>

<span data-ttu-id="06e67-115">Функция [RTFSync](rtfsync.md) вычисляет контрольную СУММУ с использованием только знаки, которые считаются важными к сообщению.</span><span class="sxs-lookup"><span data-stu-id="06e67-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="06e67-116">Например некоторые пробелов и других допускающие игнорирование символы представлены в контрольную СУММУ.</span><span class="sxs-lookup"><span data-stu-id="06e67-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="06e67-117">Это свойство является свойством дополнительный форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="06e67-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="06e67-118">Эти свойства, используемые функцией **RTFSync** и не предназначен для непосредственного использования в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="06e67-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06e67-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="06e67-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06e67-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="06e67-120">Protocol specifications</span></span>

<span data-ttu-id="06e67-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06e67-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06e67-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="06e67-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06e67-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06e67-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06e67-124">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="06e67-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06e67-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="06e67-125">Header files</span></span>

<span data-ttu-id="06e67-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06e67-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="06e67-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="06e67-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="06e67-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06e67-128">Mapitags.h</span></span>
  
> <span data-ttu-id="06e67-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="06e67-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06e67-130">См. также</span><span class="sxs-lookup"><span data-stu-id="06e67-130">See also</span></span>



[<span data-ttu-id="06e67-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06e67-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06e67-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06e67-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06e67-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="06e67-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06e67-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="06e67-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

