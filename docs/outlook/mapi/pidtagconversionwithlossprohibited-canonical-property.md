---
title: Каноническое свойство PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5d9261a9f33d77d52cfd6e448e69a2c1e8df415
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585236"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="e6967-103">Каноническое свойство PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="e6967-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="e6967-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6967-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6967-105">Содержит значение TRUE, если сообщение передачи (агента) — это могут выполнять сообщение преобразования текста, которые потерю данных.</span><span class="sxs-lookup"><span data-stu-id="e6967-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6967-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e6967-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e6967-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="e6967-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="e6967-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e6967-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e6967-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="e6967-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="e6967-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e6967-110">Data type:</span></span>  <br/> |<span data-ttu-id="e6967-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e6967-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e6967-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e6967-112">Area:</span></span>  <br/> |<span data-ttu-id="e6967-113">Общие настройки</span><span class="sxs-lookup"><span data-stu-id="e6967-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6967-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e6967-114">Remarks</span></span>

<span data-ttu-id="e6967-115">Пример типа преобразования запрещено — это сопоставление «с потерей данных» в кодировке Юникод (два байта на знак) в набор однобайтовых знаков.</span><span class="sxs-lookup"><span data-stu-id="e6967-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e6967-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e6967-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e6967-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e6967-117">Header files</span></span>

<span data-ttu-id="e6967-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e6967-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e6967-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e6967-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e6967-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e6967-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e6967-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e6967-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e6967-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e6967-122">See also</span></span>



[<span data-ttu-id="e6967-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e6967-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e6967-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e6967-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e6967-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e6967-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e6967-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e6967-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

