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
# <a name="pidtagserviceentryname-canonical-property"></a><span data-ttu-id="3965c-103">Каноническое свойство PidTagServiceEntryName</span><span class="sxs-lookup"><span data-stu-id="3965c-103">PidTagServiceEntryName Canonical Property</span></span>

  
  
<span data-ttu-id="3965c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3965c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3965c-105">Содержит имя функции точки входа для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3965c-105">Contains the name of the entry point function for configuration of a message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3965c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3965c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3965c-107">ПР_СЕРВИЦЕ_ЕНТРИ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="3965c-107">PR_SERVICE_ENTRY_NAME</span></span>  <br/> |
|<span data-ttu-id="3965c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3965c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3965c-109">0x3D0B</span><span class="sxs-lookup"><span data-stu-id="3965c-109">0x3D0B</span></span>  <br/> |
|<span data-ttu-id="3965c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3965c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3965c-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3965c-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3965c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3965c-112">Area:</span></span>  <br/> |<span data-ttu-id="3965c-113">Профиль MAPI</span><span class="sxs-lookup"><span data-stu-id="3965c-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3965c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3965c-114">Remarks</span></span>

<span data-ttu-id="3965c-115">Рекомендуется, чтобы разработчики службы сообщений предоставляли точку входа в службу сообщений, но точка входа не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="3965c-115">It is recommended that message service implementers provide a message service entry point, but the entry point is not required.</span></span> <span data-ttu-id="3965c-116">Однако точка входа должна быть указана только в том случае, если существуют связанные свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3965c-116">However, the entry point should be supplied only if the related configuration properties exist.</span></span> <span data-ttu-id="3965c-117">Если эти свойства не существуют, MAPI предполагает, что точка входа не указана.</span><span class="sxs-lookup"><span data-stu-id="3965c-117">If these properties do not exist, MAPI assumes that no entry point is provided.</span></span>
  
<span data-ttu-id="3965c-118">Библиотека динамической компоновки (DLL), в которой отображается функция точки входа, называется свойством **пр_сервице_длл_наме** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3965c-118">The dynamic-link library (DLL) in which the entry point function appears is named by the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="3965c-119">Для получения дополнительных сведений о точках входа в службу сообщений, ознакомьтесь со статьей [Реализация функции точки входа поставщика услуг](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="3965c-119">For more information on message service entry points, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3965c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3965c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3965c-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="3965c-121">Header files</span></span>

<span data-ttu-id="3965c-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3965c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3965c-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3965c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3965c-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="3965c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3965c-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="3965c-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3965c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3965c-126">See also</span></span>



[<span data-ttu-id="3965c-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3965c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3965c-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="3965c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3965c-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3965c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3965c-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3965c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

