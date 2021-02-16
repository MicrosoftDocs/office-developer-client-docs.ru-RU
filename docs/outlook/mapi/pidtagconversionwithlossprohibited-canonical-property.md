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
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417128"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="2ea62-103">Каноническое свойство PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="2ea62-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="2ea62-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ea62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ea62-105">Содержит true, если агенту передачи сообщений запрещено преобразование текста сообщения, которое теряет сведения.</span><span class="sxs-lookup"><span data-stu-id="2ea62-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ea62-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2ea62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ea62-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="2ea62-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="2ea62-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2ea62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ea62-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="2ea62-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="2ea62-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2ea62-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ea62-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2ea62-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2ea62-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2ea62-112">Area:</span></span>  <br/> |<span data-ttu-id="2ea62-113">Общая конфигурация</span><span class="sxs-lookup"><span data-stu-id="2ea62-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ea62-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ea62-114">Remarks</span></span>

<span data-ttu-id="2ea62-115">В качестве примера запрещенного типа преобразования можно привести сопоставление "lossy" из Юникода (два на символ) в однобайтовом наборе символов.</span><span class="sxs-lookup"><span data-stu-id="2ea62-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2ea62-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ea62-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ea62-117">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="2ea62-117">Header files</span></span>

<span data-ttu-id="2ea62-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ea62-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ea62-119">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2ea62-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ea62-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ea62-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2ea62-121">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2ea62-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ea62-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2ea62-122">See also</span></span>



[<span data-ttu-id="2ea62-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea62-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ea62-124">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea62-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ea62-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea62-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ea62-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2ea62-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

