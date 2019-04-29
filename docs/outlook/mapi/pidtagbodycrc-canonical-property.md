---
title: Каноническое свойство PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415182"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="70f2f-103">Каноническое свойство PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="70f2f-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="70f2f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f2f-105">Содержит циклическую проверку избыточности (CRC) текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="70f2f-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70f2f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="70f2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70f2f-107">ПР_БОДИ_КРК</span><span class="sxs-lookup"><span data-stu-id="70f2f-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="70f2f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="70f2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70f2f-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="70f2f-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="70f2f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="70f2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="70f2f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="70f2f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="70f2f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="70f2f-112">Area:</span></span>  <br/> |<span data-ttu-id="70f2f-113">Exchange;</span><span class="sxs-lookup"><span data-stu-id="70f2f-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70f2f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="70f2f-114">Remarks</span></span>

<span data-ttu-id="70f2f-115">Хранилище сообщений может использовать любой алгоритм CRC, который создает значение ПТ_ЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="70f2f-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="70f2f-116">Это свойство должно быть вычислено в составе метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , если свойство **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) задано в первый раз и когда оно было изменено позже.</span><span class="sxs-lookup"><span data-stu-id="70f2f-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="70f2f-117">Клиентское приложение использует **пр_боди_крк** для упрощения сравнения текстовых строк сообщений, которые хранятся в свойствах **пр_боди** или их вариантах.</span><span class="sxs-lookup"><span data-stu-id="70f2f-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="70f2f-118">С помощью этого свойства клиент может быстро и легко обнаружить, когда изменился текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="70f2f-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="70f2f-119">Использование **пр_боди_крк** вместо получения **пр_боди** из хранилища сообщений и его сравнения с локальной версией может значительно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="70f2f-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70f2f-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="70f2f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="70f2f-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="70f2f-121">Header files</span></span>

<span data-ttu-id="70f2f-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="70f2f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="70f2f-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="70f2f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="70f2f-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="70f2f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="70f2f-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="70f2f-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70f2f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="70f2f-126">See also</span></span>



[<span data-ttu-id="70f2f-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70f2f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70f2f-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="70f2f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70f2f-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="70f2f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70f2f-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="70f2f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

