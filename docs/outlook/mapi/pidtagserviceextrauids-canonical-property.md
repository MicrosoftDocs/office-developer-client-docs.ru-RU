---
title: Каноническое свойство PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0deb1b34a437d47ab53cdb2e13cda006d9116f65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570123"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="20ae1-103">Каноническое свойство PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="20ae1-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="20ae1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20ae1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20ae1-105">Содержит список структур [MAPIUID](mapiuid.md) , чтобы указать дополнительный профиль разделы для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="20ae1-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20ae1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="20ae1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20ae1-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="20ae1-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="20ae1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="20ae1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20ae1-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="20ae1-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="20ae1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="20ae1-110">Data type:</span></span>  <br/> |<span data-ttu-id="20ae1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="20ae1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="20ae1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="20ae1-112">Area:</span></span>  <br/> |<span data-ttu-id="20ae1-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="20ae1-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20ae1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="20ae1-114">Remarks</span></span>

<span data-ttu-id="20ae1-115">Можно создавать новые разделы профиль для каждого фильтра сообщений.</span><span class="sxs-lookup"><span data-stu-id="20ae1-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="20ae1-116">При со сведениями о службе сообщений для копирования в другой профиль необходимость копирования в разделах дополнительный профиль для фильтров также.</span><span class="sxs-lookup"><span data-stu-id="20ae1-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="20ae1-117">Поставщик службы, который использует разделах дополнительных профилей можно хранить структур **MAPIUID** разделам профилей в **PR_SERVICE_EXTRA_UIDS**, что позволяет MAPI для копирования сведений о службе дополнительное сообщение.</span><span class="sxs-lookup"><span data-stu-id="20ae1-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20ae1-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20ae1-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="20ae1-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="20ae1-119">Header files</span></span>

<span data-ttu-id="20ae1-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20ae1-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="20ae1-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="20ae1-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="20ae1-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20ae1-122">Mapitags.h</span></span>
  
> <span data-ttu-id="20ae1-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="20ae1-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20ae1-124">См. также</span><span class="sxs-lookup"><span data-stu-id="20ae1-124">See also</span></span>



[<span data-ttu-id="20ae1-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="20ae1-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20ae1-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="20ae1-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20ae1-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="20ae1-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20ae1-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="20ae1-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

