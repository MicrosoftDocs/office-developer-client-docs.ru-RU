---
title: Каноническое свойство PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346608"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="543b6-103">Каноническое свойство PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="543b6-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="543b6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="543b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="543b6-105">Содержит значение TRUE, если агенту передачи сообщений (MTA) запрещено делать неявные преобразования текста сообщений.</span><span class="sxs-lookup"><span data-stu-id="543b6-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="543b6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="543b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="543b6-107">ПР_ИМПЛИЦИТ_КОНВЕРСИОН_ПРОХИБИТЕД</span><span class="sxs-lookup"><span data-stu-id="543b6-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="543b6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="543b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="543b6-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="543b6-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="543b6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="543b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="543b6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="543b6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="543b6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="543b6-112">Area:</span></span>  <br/> |<span data-ttu-id="543b6-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="543b6-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="543b6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="543b6-114">Remarks</span></span>

<span data-ttu-id="543b6-115">Если это свойство имеет значение TRUE, система обмена сообщениями не должна выполнять преобразование содержимого для сообщения, если оно не было явно запрошено для каждого получателя с помощью свойства **пр_експлиЦит_конверсион** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="543b6-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="543b6-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="543b6-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="543b6-117">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="543b6-117">Header files</span></span>

<span data-ttu-id="543b6-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="543b6-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="543b6-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="543b6-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="543b6-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="543b6-120">Mapitags.h</span></span>
  
> <span data-ttu-id="543b6-121">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="543b6-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="543b6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="543b6-122">See also</span></span>



[<span data-ttu-id="543b6-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="543b6-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="543b6-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="543b6-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="543b6-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="543b6-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="543b6-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="543b6-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

