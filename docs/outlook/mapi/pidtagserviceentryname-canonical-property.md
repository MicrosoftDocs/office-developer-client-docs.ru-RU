---
title: Каноническое свойство PidTagServiceEntryName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3988596cc0b9c01d526354dabef3a6e7fdefc3b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583227"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="7744f-103">Каноническое свойство PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="7744f-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="7744f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7744f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7744f-105">Содержит имя функции точки входа для конфигурации службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7744f-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7744f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7744f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7744f-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="7744f-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="7744f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7744f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7744f-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="7744f-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="7744f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7744f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7744f-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7744f-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7744f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7744f-112">Area:</span></span>  <br/> |<span data-ttu-id="7744f-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="7744f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7744f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7744f-114">Remarks</span></span>

<span data-ttu-id="7744f-115">Рекомендуется специалистов по внедрению службы сообщений предоставляют точка входа службы сообщение, что точка входа не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7744f-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="7744f-116">Тем не менее точка входа должен задаваться только в том случае, если существует связанных с ними конфигурационные свойства.</span><span class="sxs-lookup"><span data-stu-id="7744f-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="7744f-117">Если эти свойства не существует, MAPI предполагает, что точка входа не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="7744f-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="7744f-118">Библиотека динамической компоновки (DLL), в котором содержится функция точки входа называется свойством **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7744f-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7744f-119">Дополнительные сведения о точки входа службы сообщений [реализации функции точки входа поставщика службы](implementing-a-service-provider-entry-point-function.md)см.</span><span class="sxs-lookup"><span data-stu-id="7744f-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7744f-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7744f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7744f-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7744f-121">Header files</span></span>

<span data-ttu-id="7744f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7744f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7744f-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7744f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7744f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7744f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7744f-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7744f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7744f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7744f-126">See also</span></span>



[<span data-ttu-id="7744f-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7744f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7744f-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7744f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7744f-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7744f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7744f-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7744f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

