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
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811930"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="48057-103">Каноническое свойство PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="48057-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="48057-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48057-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48057-105">Содержит структуру [MAPIUID](mapiuid.md) для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="48057-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48057-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="48057-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48057-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="48057-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="48057-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="48057-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48057-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="48057-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="48057-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="48057-110">Data type:</span></span>  <br/> |<span data-ttu-id="48057-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48057-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48057-112">Область:</span><span class="sxs-lookup"><span data-stu-id="48057-112">Area:</span></span>  <br/> |<span data-ttu-id="48057-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="48057-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48057-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="48057-114">Remarks</span></span>

<span data-ttu-id="48057-115">Это свойство вычисляется путем MAPI на объекты раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="48057-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="48057-116">MAPI используется для группирования всех поставщиков, относящихся к одной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="48057-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="48057-117">Это свойство предоставляется в качестве параметра Большинство методов [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="48057-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="48057-118">Он должен отображаться в Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="48057-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48057-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="48057-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="48057-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="48057-120">Header files</span></span>

<span data-ttu-id="48057-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48057-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="48057-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="48057-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="48057-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48057-123">Mapitags.h</span></span>
  
> <span data-ttu-id="48057-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="48057-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48057-125">См. также</span><span class="sxs-lookup"><span data-stu-id="48057-125">See also</span></span>



[<span data-ttu-id="48057-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48057-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="48057-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48057-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48057-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48057-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48057-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="48057-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48057-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="48057-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

