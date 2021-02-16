---
title: Каноническое свойство PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439844"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="c9155-103">Каноническое свойство PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="c9155-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="c9155-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9155-105">Это свойство содержит число, которое указывает состояние удаленной передачи.</span><span class="sxs-lookup"><span data-stu-id="c9155-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9155-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c9155-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9155-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="c9155-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="c9155-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c9155-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9155-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="c9155-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="c9155-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c9155-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9155-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c9155-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c9155-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c9155-112">Area:</span></span>  <br/> |<span data-ttu-id="c9155-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="c9155-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9155-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9155-114">Remarks</span></span>

<span data-ttu-id="c9155-115">Если передача не идет, этому свойству следует установить 1.</span><span class="sxs-lookup"><span data-stu-id="c9155-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="c9155-116">Если передача идет, необходимо установить значение от 0 до 100, указывающее процент завершения передачи.</span><span class="sxs-lookup"><span data-stu-id="c9155-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="c9155-117">Текст, связанный с числовым кодом состояния, отображается в свойстве **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText).](pidtagremoteprogresstext-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c9155-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c9155-118">Для этого свойства можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c9155-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="c9155-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="c9155-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="c9155-120">Передача сообщений удаляется.</span><span class="sxs-lookup"><span data-stu-id="c9155-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="c9155-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="c9155-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="c9155-122">Передача сообщений идет.</span><span class="sxs-lookup"><span data-stu-id="c9155-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c9155-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c9155-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9155-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c9155-124">Header files</span></span>

<span data-ttu-id="c9155-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9155-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9155-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c9155-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9155-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9155-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c9155-128">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="c9155-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9155-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c9155-129">See also</span></span>



[<span data-ttu-id="c9155-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c9155-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9155-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c9155-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9155-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c9155-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9155-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c9155-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

