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
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="06c27-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="06c27-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="06c27-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06c27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06c27-105">Указывает, включен ли режим кэшации Exchange для папки "Избранное общедоступных папок" и является ли этот режим принудительно применен политикой. </span><span class="sxs-lookup"><span data-stu-id="06c27-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="06c27-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="06c27-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06c27-107">Экспортируется по:</span><span class="sxs-lookup"><span data-stu-id="06c27-107">Exported by:</span></span>  <br/> |<span data-ttu-id="06c27-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="06c27-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="06c27-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="06c27-109">Called by:</span></span>  <br/> |<span data-ttu-id="06c27-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="06c27-110">Client</span></span>  <br/> |
|<span data-ttu-id="06c27-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="06c27-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="06c27-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="06c27-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="06c27-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="06c27-113">Parameters</span></span>

 <span data-ttu-id="06c27-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="06c27-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="06c27-115">[out] имеет значение **true,** если возвращаемого значения принудительно политики, **false,** если это не так.</span><span class="sxs-lookup"><span data-stu-id="06c27-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="06c27-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="06c27-116">Return values</span></span>

 <span data-ttu-id="06c27-117">**true**</span><span class="sxs-lookup"><span data-stu-id="06c27-117">**true**</span></span>
  
- <span data-ttu-id="06c27-118">Кэшинг включен.</span><span class="sxs-lookup"><span data-stu-id="06c27-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="06c27-119">**false**</span><span class="sxs-lookup"><span data-stu-id="06c27-119">**false**</span></span>
  
- <span data-ttu-id="06c27-120">Кэшинг отключен.</span><span class="sxs-lookup"><span data-stu-id="06c27-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06c27-121">См. также</span><span class="sxs-lookup"><span data-stu-id="06c27-121">See also</span></span>



[<span data-ttu-id="06c27-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="06c27-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

