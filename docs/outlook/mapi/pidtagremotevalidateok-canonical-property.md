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
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424226"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="037db-103">Каноническое свойство PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="037db-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="037db-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="037db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="037db-105">Это свойство содержит значение TRUE, если удаленному средству просмотра разрешено вызывать метод [имапистатус:: валидатестате](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="037db-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="037db-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="037db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="037db-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="037db-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="037db-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="037db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="037db-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="037db-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="037db-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="037db-110">Data type:</span></span>  <br/> |<span data-ttu-id="037db-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="037db-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="037db-112">Область:</span><span class="sxs-lookup"><span data-stu-id="037db-112">Area:</span></span>  <br/> |<span data-ttu-id="037db-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="037db-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="037db-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="037db-114">Remarks</span></span>

<span data-ttu-id="037db-115">Это свойство отображается в таблице состояние и предоставляет некоторый контроль над производительностью транспорта.</span><span class="sxs-lookup"><span data-stu-id="037db-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="037db-116">Его можно рассматривать как другой способ, позволяющий удаленному средству просмотра переключаться в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="037db-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="037db-117">Если задано значение TRUE, удаленное средство просмотра может вызывать **имапистатус:: валидатестате** как можно чаще.</span><span class="sxs-lookup"><span data-stu-id="037db-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="037db-118">Значение FALSE указывает на то, что удаленное средство просмотра не может совершать другие вызовы.</span><span class="sxs-lookup"><span data-stu-id="037db-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="037db-119">Поставщик транспорта обычно задает это свойство динамически, устанавливая значение FALSE, чтобы отключить дополнительные вызовы, когда у поставщика транспорта достаточно объема обработки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="037db-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="037db-120">После завершения работы поставщика транспорта устанавливается значение TRUE, чтобы разрешить клиентскому приложению выполнять дальнейшие **действия имапистатус:: валидатестате** Calls.</span><span class="sxs-lookup"><span data-stu-id="037db-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="037db-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="037db-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="037db-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="037db-122">Header files</span></span>

<span data-ttu-id="037db-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="037db-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="037db-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="037db-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="037db-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="037db-125">Mapitags.h</span></span>
  
> <span data-ttu-id="037db-126">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="037db-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="037db-127">См. также</span><span class="sxs-lookup"><span data-stu-id="037db-127">See also</span></span>



[<span data-ttu-id="037db-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="037db-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="037db-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="037db-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="037db-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="037db-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="037db-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="037db-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

