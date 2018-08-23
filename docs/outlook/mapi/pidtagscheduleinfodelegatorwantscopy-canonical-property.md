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
ms.openlocfilehash: c37f5a3e2f1a5ec4411f2570d8a3fcdce52dfe57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578649"
---
# <a name="pidtagscheduleinfodelegatorwantscopy-canonical-property"></a><span data-ttu-id="97c71-103">Каноническое свойство PidTagScheduleInfoDelegatorWantsCopy</span><span class="sxs-lookup"><span data-stu-id="97c71-103">PidTagScheduleInfoDelegatorWantsCopy Canonical Property</span></span>

  
  
<span data-ttu-id="97c71-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97c71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97c71-105">Содержит значение TRUE, если представитель может принимать копии объектов связанные собрания, отправляемые на делегат.</span><span class="sxs-lookup"><span data-stu-id="97c71-105">Contains TRUE if the delegator wants to receive copies of the meeting-related objects that are sent to the delegate.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97c71-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="97c71-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97c71-107">PR_SCHDINFO_BOSS_WANTS_COPY</span><span class="sxs-lookup"><span data-stu-id="97c71-107">PR_SCHDINFO_BOSS_WANTS_COPY</span></span>  <br/> |
|<span data-ttu-id="97c71-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="97c71-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97c71-109">0x6842</span><span class="sxs-lookup"><span data-stu-id="97c71-109">0x6842</span></span>  <br/> |
|<span data-ttu-id="97c71-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="97c71-110">Data type:</span></span>  <br/> |<span data-ttu-id="97c71-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="97c71-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="97c71-112">Область:</span><span class="sxs-lookup"><span data-stu-id="97c71-112">Area:</span></span>  <br/> |<span data-ttu-id="97c71-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="97c71-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97c71-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="97c71-114">Remarks</span></span>

<span data-ttu-id="97c71-115">Это свойство необходимо установить в объекте сведения делегата.</span><span class="sxs-lookup"><span data-stu-id="97c71-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97c71-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97c71-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97c71-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="97c71-117">Protocol specifications</span></span>

<span data-ttu-id="97c71-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97c71-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97c71-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="97c71-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="97c71-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97c71-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97c71-121">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="97c71-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="97c71-122">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97c71-122">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97c71-123">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="97c71-123">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97c71-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="97c71-124">Header files</span></span>

<span data-ttu-id="97c71-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97c71-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="97c71-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="97c71-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="97c71-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97c71-127">Mapitags.h</span></span>
  
> <span data-ttu-id="97c71-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="97c71-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97c71-129">См. также</span><span class="sxs-lookup"><span data-stu-id="97c71-129">See also</span></span>



[<span data-ttu-id="97c71-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97c71-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97c71-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97c71-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97c71-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="97c71-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97c71-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="97c71-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

