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
ms.openlocfilehash: 6f78609537b85a89617e7b2fa8f30a4ba952805b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414811"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a><span data-ttu-id="e8752-103">Каноническое свойство PidTagOriginatingMtaCertificate</span><span class="sxs-lookup"><span data-stu-id="e8752-103">PidTagOriginatingMtaCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="e8752-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8752-105">Содержит идентификатор агента передачи сообщений (MTA), зародив сообщение.</span><span class="sxs-lookup"><span data-stu-id="e8752-105">Contains an identifier for the message transfer agent (MTA) that originated the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8752-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e8752-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8752-107">PR_ORIGINATING_MTA_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="e8752-107">PR_ORIGINATING_MTA_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="e8752-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e8752-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8752-109">0x0E25</span><span class="sxs-lookup"><span data-stu-id="e8752-109">0x0E25</span></span>  <br/> |
|<span data-ttu-id="e8752-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e8752-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8752-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e8752-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e8752-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e8752-112">Area:</span></span>  <br/> |<span data-ttu-id="e8752-113">Server</span><span class="sxs-lookup"><span data-stu-id="e8752-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8752-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8752-114">Remarks</span></span>

<span data-ttu-id="e8752-115">Это свойство, если установлено, доступно для отправленных сообщений в папке Отправленные элементы.</span><span class="sxs-lookup"><span data-stu-id="e8752-115">This property, if set, is available on sent messages in the Sent Items folder.</span></span>
  
<span data-ttu-id="e8752-116">Это свойство соответствует атрибуту отчета X.400 за сообщение.</span><span class="sxs-lookup"><span data-stu-id="e8752-116">This property corresponds to the X.400 report per-message attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8752-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e8752-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8752-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e8752-118">Header files</span></span>

<span data-ttu-id="e8752-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8752-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8752-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e8752-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8752-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e8752-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e8752-122">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="e8752-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8752-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e8752-123">See also</span></span>



[<span data-ttu-id="e8752-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e8752-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8752-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e8752-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8752-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e8752-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8752-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e8752-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

