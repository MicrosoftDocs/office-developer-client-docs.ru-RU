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
ms.openlocfilehash: 4e6495d5521e0f277ac4d501a987de0142d0960d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811693"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="a1ec8-103">Каноническое свойство PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="a1ec8-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="a1ec8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1ec8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1ec8-105">Это свойство содержит число, указывающее состояние удаленной передачи.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1ec8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a1ec8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1ec8-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="a1ec8-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="a1ec8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a1ec8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1ec8-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="a1ec8-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="a1ec8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a1ec8-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1ec8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a1ec8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a1ec8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a1ec8-112">Area:</span></span>  <br/> |<span data-ttu-id="a1ec8-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ec8-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1ec8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1ec8-114">Remarks</span></span>

<span data-ttu-id="a1ec8-115">Если передача не находится в стадии разработки, это свойство необходимо задать значение 1.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="a1ec8-116">При передаче находится в стадии разработки, оно должно быть присвоено значение от 0 до 100, указывающее процент завершения переноса.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="a1ec8-117">Текст, связанный с кодом числовое состояние отображается в свойстве **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a1ec8-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a1ec8-118">Следующие флаги можно задать для этого свойства:</span><span class="sxs-lookup"><span data-stu-id="a1ec8-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="a1ec8-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a1ec8-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="a1ec8-120">Передача сообщений будет удален.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="a1ec8-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a1ec8-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="a1ec8-122">Передача сообщений находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a1ec8-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a1ec8-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a1ec8-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a1ec8-124">Header files</span></span>

<span data-ttu-id="a1ec8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1ec8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1ec8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1ec8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a1ec8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a1ec8-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a1ec8-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1ec8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a1ec8-129">See also</span></span>



[<span data-ttu-id="a1ec8-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ec8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1ec8-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ec8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1ec8-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a1ec8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1ec8-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a1ec8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

