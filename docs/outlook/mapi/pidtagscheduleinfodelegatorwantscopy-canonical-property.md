---
title: Каноническое свойство PidTagScheduleInfoDelegatorWantsCopy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegatorWantsCopy
api_type:
- COM
ms.assetid: 48e48e3a-1186-46c4-8ff9-34e03905fb93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c52a1c055792f17477ff5540c4138160544e3b18
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400427"
---
# <a name="pidtagscheduleinfodelegatorwantscopy-canonical-property"></a><span data-ttu-id="f0e8c-103">Каноническое свойство PidTagScheduleInfoDelegatorWantsCopy</span><span class="sxs-lookup"><span data-stu-id="f0e8c-103">PidTagScheduleInfoDelegatorWantsCopy Canonical Property</span></span>

  
  
<span data-ttu-id="f0e8c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0e8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0e8c-105">Содержит значение TRUE, если представитель может принимать копии объектов связанные собрания, отправляемые на делегат.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-105">Contains TRUE if the delegator wants to receive copies of the meeting-related objects that are sent to the delegate.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0e8c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f0e8c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0e8c-107">PR_SCHDINFO_BOSS_WANTS_COPY</span><span class="sxs-lookup"><span data-stu-id="f0e8c-107">PR_SCHDINFO_BOSS_WANTS_COPY</span></span>  <br/> |
|<span data-ttu-id="f0e8c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f0e8c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0e8c-109">0x6842</span><span class="sxs-lookup"><span data-stu-id="f0e8c-109">0x6842</span></span>  <br/> |
|<span data-ttu-id="f0e8c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f0e8c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0e8c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f0e8c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f0e8c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f0e8c-112">Area:</span></span>  <br/> |<span data-ttu-id="f0e8c-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="f0e8c-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0e8c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0e8c-114">Remarks</span></span>

<span data-ttu-id="f0e8c-115">Это свойство необходимо установить в объекте сведения делегата.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f0e8c-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f0e8c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0e8c-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f0e8c-117">Protocol specifications</span></span>

<span data-ttu-id="f0e8c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0e8c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0e8c-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0e8c-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0e8c-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0e8c-121">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="f0e8c-122">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0e8c-122">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0e8c-123">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-123">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0e8c-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f0e8c-124">Header files</span></span>

<span data-ttu-id="f0e8c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0e8c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0e8c-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0e8c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0e8c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f0e8c-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f0e8c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0e8c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f0e8c-129">See also</span></span>



[<span data-ttu-id="f0e8c-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f0e8c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0e8c-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f0e8c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0e8c-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f0e8c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0e8c-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f0e8c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

