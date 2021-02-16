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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357871"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="a24ce-103">Каноническое свойство PidTagRtfSyncBodyCrc</span><span class="sxs-lookup"><span data-stu-id="a24ce-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="a24ce-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a24ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a24ce-105">Содержит циклическую проверку избыточности (CRC), вычисленную для текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="a24ce-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a24ce-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a24ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a24ce-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="a24ce-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="a24ce-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a24ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a24ce-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="a24ce-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="a24ce-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a24ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="a24ce-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a24ce-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a24ce-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a24ce-112">Area:</span></span>  <br/> |<span data-ttu-id="a24ce-113">Сообщение MAPI</span><span class="sxs-lookup"><span data-stu-id="a24ce-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a24ce-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a24ce-114">Remarks</span></span>

<span data-ttu-id="a24ce-115">Функция [RTFSync](rtfsync.md) вычисляет CRC, используя только символы, которые она считает значимыми для сообщения.</span><span class="sxs-lookup"><span data-stu-id="a24ce-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="a24ce-116">Например, некоторые пробелы и другие игнорируемые символы опущены из CRC.</span><span class="sxs-lookup"><span data-stu-id="a24ce-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="a24ce-117">Это свойство является вспомогательным свойством RTF.</span><span class="sxs-lookup"><span data-stu-id="a24ce-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="a24ce-118">Эти свойства используются функцией **RTFSync** и не предназначены для непосредственного использования клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="a24ce-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a24ce-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a24ce-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a24ce-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a24ce-120">Protocol specifications</span></span>

<span data-ttu-id="a24ce-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a24ce-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a24ce-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a24ce-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a24ce-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a24ce-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a24ce-124">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="a24ce-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a24ce-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="a24ce-125">Header files</span></span>

<span data-ttu-id="a24ce-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a24ce-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a24ce-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a24ce-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a24ce-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a24ce-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a24ce-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a24ce-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a24ce-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a24ce-130">See also</span></span>



[<span data-ttu-id="a24ce-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a24ce-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a24ce-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a24ce-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a24ce-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a24ce-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a24ce-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a24ce-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

