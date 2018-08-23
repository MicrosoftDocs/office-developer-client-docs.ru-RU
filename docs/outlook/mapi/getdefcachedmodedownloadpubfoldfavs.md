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
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581729"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="3307f-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="3307f-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="3307f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3307f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3307f-105">Указывает, включена ли режима кэширования данных Exchange для **Общей папки "Избранное"** папки и ли это требование политики.</span><span class="sxs-lookup"><span data-stu-id="3307f-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3307f-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3307f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3307f-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="3307f-107">Exported by:</span></span>  <br/> |<span data-ttu-id="3307f-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="3307f-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="3307f-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="3307f-109">Called by:</span></span>  <br/> |<span data-ttu-id="3307f-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="3307f-110">Client</span></span>  <br/> |
|<span data-ttu-id="3307f-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="3307f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3307f-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="3307f-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="3307f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="3307f-113">Parameters</span></span>

 <span data-ttu-id="3307f-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="3307f-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="3307f-115">[out] **значение true,** Если возвращаемое значение обеспечивается политики **значение false** , если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="3307f-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3307f-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3307f-116">Return values</span></span>

 <span data-ttu-id="3307f-117">**значение true**</span><span class="sxs-lookup"><span data-stu-id="3307f-117">**true**</span></span>
  
- <span data-ttu-id="3307f-118">Кэширование.</span><span class="sxs-lookup"><span data-stu-id="3307f-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="3307f-119">**false**</span><span class="sxs-lookup"><span data-stu-id="3307f-119">**false**</span></span>
  
- <span data-ttu-id="3307f-120">Кэширование отключено.</span><span class="sxs-lookup"><span data-stu-id="3307f-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3307f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="3307f-121">See also</span></span>



[<span data-ttu-id="3307f-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="3307f-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

