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
ms.openlocfilehash: 2c771f1d97305271b70102c148e62f30512974fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432473"
---
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="93335-103">Каноническое свойство PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="93335-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="93335-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93335-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93335-105">Содержит имя функции точки входа для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="93335-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93335-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="93335-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93335-107">PR_SERVICE_ENTRY_NAME</span><span class="sxs-lookup"><span data-stu-id="93335-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="93335-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="93335-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93335-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="93335-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="93335-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="93335-110">Data type:</span></span>  <br/> |<span data-ttu-id="93335-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="93335-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="93335-112">Область:</span><span class="sxs-lookup"><span data-stu-id="93335-112">Area:</span></span>  <br/> |<span data-ttu-id="93335-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="93335-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93335-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="93335-114">Remarks</span></span>

<span data-ttu-id="93335-115">Рекомендуется, чтобы реализутели службы сообщений предоставили точку входа в службу сообщений, но точка входа не требуется.</span><span class="sxs-lookup"><span data-stu-id="93335-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="93335-116">Однако точка входа должна быть поставлена только в том случае, если существуют соответствующие свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="93335-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="93335-117">Если эти свойства не существуют, MAPI предполагает, что точка входа не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="93335-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="93335-118">Библиотека динамических ссылок (DLL), в которой отображается функция **точки входа,** называется свойством [PR_SERVICE_DLL_NAME (PidTagServiceDllName).](pidtagservicedllname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="93335-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="93335-119">Дополнительные сведения о точках входа в службу сообщений см. в таблице [Реализация функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="93335-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93335-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="93335-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="93335-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="93335-121">Header files</span></span>

<span data-ttu-id="93335-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93335-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="93335-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="93335-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="93335-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93335-124">Mapitags.h</span></span>
  
> <span data-ttu-id="93335-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="93335-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93335-126">См. также</span><span class="sxs-lookup"><span data-stu-id="93335-126">See also</span></span>



[<span data-ttu-id="93335-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93335-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93335-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="93335-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93335-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="93335-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93335-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="93335-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

