---
title: Каноническое свойство PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426529"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="7b2e0-103">Каноническое свойство PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="7b2e0-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="7b2e0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b2e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b2e0-105">Содержит структуру [мапиуид](mapiuid.md) для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b2e0-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b2e0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b2e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b2e0-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="7b2e0-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="7b2e0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7b2e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b2e0-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="7b2e0-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="7b2e0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b2e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b2e0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7b2e0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7b2e0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7b2e0-112">Area:</span></span>  <br/> |<span data-ttu-id="7b2e0-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="7b2e0-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b2e0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b2e0-114">Remarks</span></span>

<span data-ttu-id="7b2e0-115">Это свойство вычисляется MAPI в объектах раздела profile.</span><span class="sxs-lookup"><span data-stu-id="7b2e0-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="7b2e0-116">MAPI использует ее для группировки всех поставщиков, относящихся к одной службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="7b2e0-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="7b2e0-117">Это свойство предоставляется в качестве параметра большинству методов [имсгсервицеадмин](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7b2e0-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="7b2e0-118">Он не должен отображаться в Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="7b2e0-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b2e0-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b2e0-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7b2e0-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7b2e0-120">Header files</span></span>

<span data-ttu-id="7b2e0-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7b2e0-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b2e0-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b2e0-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b2e0-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="7b2e0-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7b2e0-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="7b2e0-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b2e0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7b2e0-125">See also</span></span>



[<span data-ttu-id="7b2e0-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b2e0-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="7b2e0-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b2e0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b2e0-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="7b2e0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b2e0-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b2e0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b2e0-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b2e0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

