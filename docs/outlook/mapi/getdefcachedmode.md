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
# <a name="getdefcachedmode"></a><span data-ttu-id="386cb-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="386cb-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="386cb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="386cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="386cb-105">Указывает, включен ли режим кэшации Exchange для частного магазина Exchange и является ли этот режим принудительно применен политикой.</span><span class="sxs-lookup"><span data-stu-id="386cb-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="386cb-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="386cb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="386cb-107">Экспортируется по:</span><span class="sxs-lookup"><span data-stu-id="386cb-107">Exported by:</span></span>  <br/> |<span data-ttu-id="386cb-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="386cb-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="386cb-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="386cb-109">Called by:</span></span>  <br/> |<span data-ttu-id="386cb-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="386cb-110">Client</span></span>  <br/> |
|<span data-ttu-id="386cb-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="386cb-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="386cb-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="386cb-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="386cb-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="386cb-113">Parameters</span></span>

 <span data-ttu-id="386cb-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="386cb-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="386cb-115">[out] имеет значение **true,** если возвращаемого значения принудительно политики, **false,** если это не так.</span><span class="sxs-lookup"><span data-stu-id="386cb-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="386cb-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="386cb-116">Return values</span></span>

 <span data-ttu-id="386cb-117">**true**</span><span class="sxs-lookup"><span data-stu-id="386cb-117">**true**</span></span>
  
- <span data-ttu-id="386cb-118">Кэшинг включен.</span><span class="sxs-lookup"><span data-stu-id="386cb-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="386cb-119">**false**</span><span class="sxs-lookup"><span data-stu-id="386cb-119">**false**</span></span>
  
- <span data-ttu-id="386cb-120">Кэшинг отключен.</span><span class="sxs-lookup"><span data-stu-id="386cb-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="386cb-121">См. также</span><span class="sxs-lookup"><span data-stu-id="386cb-121">See also</span></span>



[<span data-ttu-id="386cb-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="386cb-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

