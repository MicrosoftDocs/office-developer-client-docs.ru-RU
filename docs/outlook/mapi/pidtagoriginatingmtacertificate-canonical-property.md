---
title: Каноническое свойство PidTagOriginatingMtaCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e2f4b1fda57eb74e0573834c6e8fb443acf7ab12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563907"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a><span data-ttu-id="f0c29-103">Каноническое свойство PidTagOriginatingMtaCertificate</span><span class="sxs-lookup"><span data-stu-id="f0c29-103">PidTagOriginatingMtaCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="f0c29-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0c29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0c29-105">Содержит идентификатор сообщения передачи агента (), с которого поступило сообщение.</span><span class="sxs-lookup"><span data-stu-id="f0c29-105">Contains an identifier for the message transfer agent (MTA) that originated the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0c29-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f0c29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0c29-107">PR_ORIGINATING_MTA_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="f0c29-107">PR_ORIGINATING_MTA_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="f0c29-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f0c29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0c29-109">0x0E25</span><span class="sxs-lookup"><span data-stu-id="f0c29-109">0x0E25</span></span>  <br/> |
|<span data-ttu-id="f0c29-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f0c29-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0c29-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f0c29-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f0c29-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f0c29-112">Area:</span></span>  <br/> |<span data-ttu-id="f0c29-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="f0c29-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0c29-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0c29-114">Remarks</span></span>

<span data-ttu-id="f0c29-115">Это свойство, если задано, доступные на отправляются сообщения в папке «Отправленные».</span><span class="sxs-lookup"><span data-stu-id="f0c29-115">This property, if set, is available on sent messages in the Sent Items folder.</span></span>
  
<span data-ttu-id="f0c29-116">Это свойство соответствует атрибуту X.400 отчета-message.</span><span class="sxs-lookup"><span data-stu-id="f0c29-116">This property corresponds to the X.400 report per-message attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f0c29-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f0c29-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f0c29-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f0c29-118">Header files</span></span>

<span data-ttu-id="f0c29-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0c29-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0c29-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f0c29-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0c29-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0c29-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f0c29-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="f0c29-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0c29-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f0c29-123">See also</span></span>



[<span data-ttu-id="f0c29-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f0c29-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0c29-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f0c29-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0c29-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f0c29-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0c29-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f0c29-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

