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
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811574"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="1d45f-103">Каноническое свойство PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="1d45f-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="1d45f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d45f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d45f-105">Содержит имя профиля.</span><span class="sxs-lookup"><span data-stu-id="1d45f-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d45f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1d45f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d45f-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1d45f-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="1d45f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1d45f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d45f-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="1d45f-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="1d45f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1d45f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d45f-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d45f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1d45f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1d45f-112">Area:</span></span>  <br/> |<span data-ttu-id="1d45f-113">Настройки профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="1d45f-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d45f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d45f-114">Remarks</span></span>

<span data-ttu-id="1d45f-115">Эти свойства вычисляются поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="1d45f-115">These properties are computed by service providers.</span></span> <span data-ttu-id="1d45f-116">Реализация поставщика функции **на неизвестную запись сервиса** можно использовать эти свойства для обнаружения имя профиля.</span><span class="sxs-lookup"><span data-stu-id="1d45f-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="1d45f-117">Клиентские приложения могут использовать эти свойства как удобной альтернативы для получения имени профиля, проверив свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в строке состояния таблицы подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d45f-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="1d45f-118">Эти свойства могут быть уникальным во времени, например где профиль удаляется и более поздних версий заново с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="1d45f-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="1d45f-119">MAPI предоставляющей полностью уникальные свойства **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) в разделе жестко заданного профиля **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="1d45f-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1d45f-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d45f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1d45f-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1d45f-121">Header files</span></span>

<span data-ttu-id="1d45f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d45f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d45f-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1d45f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d45f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d45f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1d45f-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1d45f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d45f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1d45f-126">See also</span></span>



[<span data-ttu-id="1d45f-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d45f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d45f-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d45f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d45f-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1d45f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d45f-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1d45f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

