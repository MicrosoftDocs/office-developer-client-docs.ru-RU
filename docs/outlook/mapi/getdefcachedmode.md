---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412746"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="14f8f-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="14f8f-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="14f8f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14f8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14f8f-105">Указывает, включен ли режим кэширования данных Exchange для частного хранилища Exchange и является ли он принудительно примененным с помощью политики.</span><span class="sxs-lookup"><span data-stu-id="14f8f-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="14f8f-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="14f8f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14f8f-107">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="14f8f-107">Exported by:</span></span>  <br/> |<span data-ttu-id="14f8f-108">MSMapi32. dll</span><span class="sxs-lookup"><span data-stu-id="14f8f-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="14f8f-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="14f8f-109">Called by:</span></span>  <br/> |<span data-ttu-id="14f8f-110">Client</span><span class="sxs-lookup"><span data-stu-id="14f8f-110">Client</span></span>  <br/> |
|<span data-ttu-id="14f8f-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="14f8f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="14f8f-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="14f8f-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="14f8f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="14f8f-113">Parameters</span></span>

 <span data-ttu-id="14f8f-114">_пфполици_</span><span class="sxs-lookup"><span data-stu-id="14f8f-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="14f8f-115">вышли **имеет значение true** , если возвращаемое значение принудительно применяется политикой, в противном случае — **false** .</span><span class="sxs-lookup"><span data-stu-id="14f8f-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="14f8f-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="14f8f-116">Return values</span></span>

 <span data-ttu-id="14f8f-117">**относится**</span><span class="sxs-lookup"><span data-stu-id="14f8f-117">**true**</span></span>
  
- <span data-ttu-id="14f8f-118">Включено кэширование.</span><span class="sxs-lookup"><span data-stu-id="14f8f-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="14f8f-119">**значения**</span><span class="sxs-lookup"><span data-stu-id="14f8f-119">**false**</span></span>
  
- <span data-ttu-id="14f8f-120">Кэширование отключено.</span><span class="sxs-lookup"><span data-stu-id="14f8f-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14f8f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="14f8f-121">See also</span></span>



[<span data-ttu-id="14f8f-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="14f8f-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

