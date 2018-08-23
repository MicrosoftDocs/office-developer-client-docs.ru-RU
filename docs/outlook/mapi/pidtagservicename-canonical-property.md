---
title: Каноническое свойство PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d950ee21c0c4c41e84c0fe1f8104219e63f84cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592677"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="59e57-103">Каноническое свойство PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="59e57-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="59e57-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59e57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59e57-105">Содержит имя службы сообщение как набор пользователем в файла MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="59e57-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59e57-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="59e57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59e57-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="59e57-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="59e57-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="59e57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59e57-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="59e57-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="59e57-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="59e57-110">Data type:</span></span>  <br/> |<span data-ttu-id="59e57-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="59e57-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="59e57-112">Область:</span><span class="sxs-lookup"><span data-stu-id="59e57-112">Area:</span></span>  <br/> |<span data-ttu-id="59e57-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="59e57-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59e57-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="59e57-114">Remarks</span></span>

<span data-ttu-id="59e57-115">Имя, содержащихся в этих свойств для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="59e57-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="59e57-116">Текст поступает из раздела [Services] в MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="59e57-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="59e57-117">Эти свойства отображаются в виде столбцов в таблице службы сообщений и может использоваться для фильтрации служб.</span><span class="sxs-lookup"><span data-stu-id="59e57-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="59e57-118">Так как она используется для идентификации и фильтрации служб, значение не должно быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="59e57-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59e57-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59e57-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="59e57-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="59e57-120">Header files</span></span>

<span data-ttu-id="59e57-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59e57-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="59e57-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="59e57-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="59e57-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59e57-123">Mapitags.h</span></span>
  
> <span data-ttu-id="59e57-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="59e57-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59e57-125">См. также</span><span class="sxs-lookup"><span data-stu-id="59e57-125">See also</span></span>



[<span data-ttu-id="59e57-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59e57-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59e57-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59e57-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59e57-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="59e57-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59e57-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="59e57-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

