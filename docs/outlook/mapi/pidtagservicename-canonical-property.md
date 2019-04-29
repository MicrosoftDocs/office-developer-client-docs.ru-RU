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
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438962"
---
# <a name="pidtagservicename-canonical-property"></a><span data-ttu-id="77b28-103">Каноническое свойство PidTagServiceName</span><span class="sxs-lookup"><span data-stu-id="77b28-103">PidTagServiceName Canonical Property</span></span>

  
  
<span data-ttu-id="77b28-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77b28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77b28-105">Содержит имя службы сообщений, заданной пользователем в файле MapiSvc. INF.</span><span class="sxs-lookup"><span data-stu-id="77b28-105">Contains the name of a message service as set by the user in the MapiSvc.inf file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77b28-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="77b28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77b28-107">ПР_СЕРВИЦЕ_НАМЕ, ПР_СЕРВИЦЕ_НАМЕ_А, ПР_СЕРВИЦЕ_НАМЕ_В</span><span class="sxs-lookup"><span data-stu-id="77b28-107">PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="77b28-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="77b28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77b28-109">0x3D09</span><span class="sxs-lookup"><span data-stu-id="77b28-109">0x3D09</span></span>  <br/> |
|<span data-ttu-id="77b28-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="77b28-110">Data type:</span></span>  <br/> |<span data-ttu-id="77b28-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="77b28-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="77b28-112">Область:</span><span class="sxs-lookup"><span data-stu-id="77b28-112">Area:</span></span>  <br/> |<span data-ttu-id="77b28-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="77b28-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77b28-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="77b28-114">Remarks</span></span>

<span data-ttu-id="77b28-115">Имя, которое хранится в этих свойствах, относится только к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="77b28-115">The name contained in these properties is specific to the message service.</span></span> <span data-ttu-id="77b28-116">Он поступает из раздела [Services] в MapiSvc. INF.</span><span class="sxs-lookup"><span data-stu-id="77b28-116">It comes from the [Services] section in MapiSvc.inf.</span></span>
  
<span data-ttu-id="77b28-117">Эти свойства отображаются в виде столбца в таблице службы сообщений и могут использоваться для фильтрации служб.</span><span class="sxs-lookup"><span data-stu-id="77b28-117">These properties appear as a column in the message service table and can be used to filter services.</span></span> <span data-ttu-id="77b28-118">Так как он используется для идентификации и фильтрации служб, значение не должно быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="77b28-118">Because it is used to identify and filter services, the value should not be localized.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77b28-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77b28-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="77b28-120">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="77b28-120">Header files</span></span>

<span data-ttu-id="77b28-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="77b28-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="77b28-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="77b28-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="77b28-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="77b28-123">Mapitags.h</span></span>
  
> <span data-ttu-id="77b28-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="77b28-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77b28-125">См. также</span><span class="sxs-lookup"><span data-stu-id="77b28-125">See also</span></span>



[<span data-ttu-id="77b28-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="77b28-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77b28-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="77b28-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77b28-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="77b28-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77b28-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="77b28-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

