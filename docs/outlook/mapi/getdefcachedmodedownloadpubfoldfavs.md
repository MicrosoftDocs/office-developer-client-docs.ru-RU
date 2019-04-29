---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417709"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="d5d45-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="d5d45-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="d5d45-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5d45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5d45-105">Указывает, включен ли режим кэширования данных Exchange для папки избранных общеДоступных **папок** , и является ли он принудительно примененной политикой.</span><span class="sxs-lookup"><span data-stu-id="d5d45-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d5d45-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d5d45-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5d45-107">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="d5d45-107">Exported by:</span></span>  <br/> |<span data-ttu-id="d5d45-108">MSMapi32. dll</span><span class="sxs-lookup"><span data-stu-id="d5d45-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="d5d45-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d5d45-109">Called by:</span></span>  <br/> |<span data-ttu-id="d5d45-110">Client</span><span class="sxs-lookup"><span data-stu-id="d5d45-110">Client</span></span>  <br/> |
|<span data-ttu-id="d5d45-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d5d45-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5d45-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="d5d45-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="d5d45-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5d45-113">Parameters</span></span>

 <span data-ttu-id="d5d45-114">_Пфполици_</span><span class="sxs-lookup"><span data-stu-id="d5d45-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="d5d45-115">вышли **имеет значение true** , если возвращаемое значение принудительно применяется политикой, в противном случае — **false** .</span><span class="sxs-lookup"><span data-stu-id="d5d45-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d5d45-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d5d45-116">Return values</span></span>

 <span data-ttu-id="d5d45-117">**относится**</span><span class="sxs-lookup"><span data-stu-id="d5d45-117">**true**</span></span>
  
- <span data-ttu-id="d5d45-118">Включено кэширование.</span><span class="sxs-lookup"><span data-stu-id="d5d45-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="d5d45-119">**значения**</span><span class="sxs-lookup"><span data-stu-id="d5d45-119">**false**</span></span>
  
- <span data-ttu-id="d5d45-120">Кэширование отключено.</span><span class="sxs-lookup"><span data-stu-id="d5d45-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5d45-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d5d45-121">See also</span></span>



[<span data-ttu-id="d5d45-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="d5d45-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

