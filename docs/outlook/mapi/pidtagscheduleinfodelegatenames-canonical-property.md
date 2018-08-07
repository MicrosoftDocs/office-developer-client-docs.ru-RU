---
title: Каноническое свойство PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fed2b23680cd2654bbb6960e3c6be07074307a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811823"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a><span data-ttu-id="84527-103">Каноническое свойство PidTagScheduleInfoDelegateNames</span><span class="sxs-lookup"><span data-stu-id="84527-103">PidTagScheduleInfoDelegateNames Canonical Property</span></span>

  
  
<span data-ttu-id="84527-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84527-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84527-105">Содержит имена делегаты.</span><span class="sxs-lookup"><span data-stu-id="84527-105">Contains the names of the delegates.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84527-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="84527-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84527-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="84527-107">PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="84527-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="84527-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84527-109">0x6844</span><span class="sxs-lookup"><span data-stu-id="84527-109">0x6844</span></span>  <br/> |
|<span data-ttu-id="84527-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="84527-110">Data type:</span></span>  <br/> |<span data-ttu-id="84527-111">PT_MV_STRING8 PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84527-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="84527-112">Область:</span><span class="sxs-lookup"><span data-stu-id="84527-112">Area:</span></span>  <br/> |<span data-ttu-id="84527-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="84527-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84527-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="84527-114">Remarks</span></span>

<span data-ttu-id="84527-115">Каждая запись в эти свойства должно содержать значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) каждого делегата адресной книги.</span><span class="sxs-lookup"><span data-stu-id="84527-115">Each entry in these properties must contain the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each delegate's address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84527-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="84527-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84527-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="84527-117">Protocol specifications</span></span>

<span data-ttu-id="84527-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84527-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84527-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="84527-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84527-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84527-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84527-121">Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="84527-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84527-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="84527-122">Header files</span></span>

<span data-ttu-id="84527-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84527-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="84527-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="84527-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="84527-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84527-125">Mapitags.h</span></span>
  
> <span data-ttu-id="84527-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="84527-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84527-127">См. также</span><span class="sxs-lookup"><span data-stu-id="84527-127">See also</span></span>



[<span data-ttu-id="84527-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84527-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84527-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84527-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84527-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="84527-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84527-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="84527-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

