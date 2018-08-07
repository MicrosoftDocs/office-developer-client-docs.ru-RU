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
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811232"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="67041-103">Каноническое свойство PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="67041-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="67041-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="67041-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="67041-105">Содержит значение TRUE, если сообщение передачи (агента) — это могут выполнять неявные сообщение преобразования текста.</span><span class="sxs-lookup"><span data-stu-id="67041-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67041-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="67041-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67041-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="67041-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="67041-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="67041-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67041-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="67041-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="67041-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="67041-110">Data type:</span></span>  <br/> |<span data-ttu-id="67041-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="67041-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="67041-112">Область:</span><span class="sxs-lookup"><span data-stu-id="67041-112">Area:</span></span>  <br/> |<span data-ttu-id="67041-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="67041-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67041-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="67041-114">Remarks</span></span>

<span data-ttu-id="67041-115">Если это свойство имеет значение TRUE, системы обмена сообщениями должен не выполняет преобразование содержимого в окне сообщения без его явного запроса на основе каждого получателя с помощью свойства **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="67041-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67041-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67041-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="67041-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="67041-117">Header files</span></span>

<span data-ttu-id="67041-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67041-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="67041-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="67041-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="67041-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67041-120">Mapitags.h</span></span>
  
> <span data-ttu-id="67041-121">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="67041-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67041-122">См. также</span><span class="sxs-lookup"><span data-stu-id="67041-122">See also</span></span>



[<span data-ttu-id="67041-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="67041-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67041-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="67041-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67041-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="67041-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67041-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="67041-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

