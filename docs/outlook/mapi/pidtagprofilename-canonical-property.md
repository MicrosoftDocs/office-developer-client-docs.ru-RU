---
title: Каноническое свойство PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341652"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="c5094-103">Каноническое свойство PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="c5094-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="c5094-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5094-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5094-105">Содержит имя профиля.</span><span class="sxs-lookup"><span data-stu-id="c5094-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5094-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5094-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5094-107">ПР_ПРОФИЛЕ_НАМЕ, ПР_ПРОФИЛЕ_НАМЕ_А, ПР_ПРОФИЛЕ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="c5094-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c5094-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c5094-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5094-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="c5094-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="c5094-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5094-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5094-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="c5094-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c5094-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c5094-112">Area:</span></span>  <br/> |<span data-ttu-id="c5094-113">Конфигурация профиля MAPI</span><span class="sxs-lookup"><span data-stu-id="c5094-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5094-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5094-114">Remarks</span></span>

<span data-ttu-id="c5094-115">Эти свойства рассчитываются поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="c5094-115">These properties are computed by service providers.</span></span> <span data-ttu-id="c5094-116">Реализация поставщика функции **сервицеентри** может использовать эти свойства для обнаружения имени профиля.</span><span class="sxs-lookup"><span data-stu-id="c5094-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="c5094-117">Клиентские приложения могут использовать эти свойства в качестве удобной альтернативы для получения имени профиля путем проверки свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в строке таблицы состояния подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5094-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="c5094-118">Эти свойства могут быть неуникальными по времени, например при удалении профиля и повторном создании с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="c5094-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="c5094-119">MAPI поменяет полностью уникальное свойство **пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) в жестко закодированном разделе профиля с именем **муид_профиле_инстанце.**</span><span class="sxs-lookup"><span data-stu-id="c5094-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5094-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5094-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c5094-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="c5094-121">Header files</span></span>

<span data-ttu-id="c5094-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c5094-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5094-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5094-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5094-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c5094-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c5094-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c5094-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5094-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c5094-126">See also</span></span>



[<span data-ttu-id="c5094-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5094-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5094-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c5094-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5094-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5094-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5094-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5094-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

