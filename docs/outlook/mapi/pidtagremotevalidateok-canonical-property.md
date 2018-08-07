---
title: Каноническое свойство PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811704"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="c915c-103">Каноническое свойство PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="c915c-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="c915c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c915c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c915c-105">Это свойство содержит значение TRUE, если удаленного просмотра может вызвать метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="c915c-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c915c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c915c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c915c-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="c915c-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="c915c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c915c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c915c-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="c915c-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="c915c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c915c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c915c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c915c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c915c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c915c-112">Area:</span></span>  <br/> |<span data-ttu-id="c915c-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="c915c-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c915c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c915c-114">Remarks</span></span>

<span data-ttu-id="c915c-115">Это свойство отображается в таблице состояния и предлагает управлять производительности транспорта.</span><span class="sxs-lookup"><span data-stu-id="c915c-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="c915c-116">Его можно рассматривать как другим способом направления удаленного просмотра для бездействующих.</span><span class="sxs-lookup"><span data-stu-id="c915c-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="c915c-117">Если он имеет значение TRUE, средство просмотра удаленных можно вызвать **IMAPIStatus::ValidateState** необходимое.</span><span class="sxs-lookup"><span data-stu-id="c915c-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="c915c-118">Значение FALSE указывает, что средство просмотра удаленных не может выполнять любые дополнительные вызовы.</span><span class="sxs-lookup"><span data-stu-id="c915c-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="c915c-119">Поставщика транспорта обычно этому свойству динамически, задав значение FALSE, чтобы отключить дополнительные вызовы, когда поставщика транспорта имеет достаточные объем обработки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="c915c-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="c915c-120">По завершении поставщика транспорта его устанавливает значение значение TRUE, чтобы разрешить клиентское приложение для дальнейшей **IMAPIStatus::ValidateState** вызовов.</span><span class="sxs-lookup"><span data-stu-id="c915c-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c915c-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c915c-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c915c-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c915c-122">Header files</span></span>

<span data-ttu-id="c915c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c915c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c915c-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c915c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c915c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c915c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c915c-126">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="c915c-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c915c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c915c-127">See also</span></span>



[<span data-ttu-id="c915c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c915c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c915c-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c915c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c915c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c915c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c915c-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c915c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

