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
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582254"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="2fe78-103">Каноническое свойство PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="2fe78-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="2fe78-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fe78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fe78-105">Содержит структуру [MAPIUID](mapiuid.md) для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2fe78-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fe78-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2fe78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2fe78-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="2fe78-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="2fe78-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2fe78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2fe78-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="2fe78-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="2fe78-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2fe78-110">Data type:</span></span>  <br/> |<span data-ttu-id="2fe78-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2fe78-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2fe78-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2fe78-112">Area:</span></span>  <br/> |<span data-ttu-id="2fe78-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe78-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fe78-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2fe78-114">Remarks</span></span>

<span data-ttu-id="2fe78-115">Это свойство вычисляется путем MAPI на объекты раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="2fe78-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="2fe78-116">MAPI используется для группирования всех поставщиков, относящихся к одной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2fe78-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="2fe78-117">Это свойство предоставляется в качестве параметра Большинство методов [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe78-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="2fe78-118">Он должен отображаться в Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="2fe78-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2fe78-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2fe78-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2fe78-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2fe78-120">Header files</span></span>

<span data-ttu-id="2fe78-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2fe78-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="2fe78-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2fe78-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="2fe78-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2fe78-123">Mapitags.h</span></span>
  
> <span data-ttu-id="2fe78-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2fe78-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fe78-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2fe78-125">See also</span></span>



[<span data-ttu-id="2fe78-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fe78-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="2fe78-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe78-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2fe78-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe78-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2fe78-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe78-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2fe78-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2fe78-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

