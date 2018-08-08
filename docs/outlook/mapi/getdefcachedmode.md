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
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808567"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="20964-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="20964-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="20964-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20964-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20964-105">Указывает, включена ли режима кэширования данных Exchange для закрытого хранилища Exchange и ли это требование политики.</span><span class="sxs-lookup"><span data-stu-id="20964-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="20964-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="20964-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20964-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="20964-107">Exported by:</span></span>  <br/> |<span data-ttu-id="20964-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="20964-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="20964-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="20964-109">Called by:</span></span>  <br/> |<span data-ttu-id="20964-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="20964-110">Client</span></span>  <br/> |
|<span data-ttu-id="20964-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="20964-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="20964-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="20964-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="20964-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="20964-113">Parameters</span></span>

 <span data-ttu-id="20964-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="20964-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="20964-115">[out] **значение true,** Если возвращаемое значение обеспечивается политики **значение false** , если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="20964-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="20964-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="20964-116">Return values</span></span>

 <span data-ttu-id="20964-117">**значение true**</span><span class="sxs-lookup"><span data-stu-id="20964-117">**true**</span></span>
  
- <span data-ttu-id="20964-118">Кэширование.</span><span class="sxs-lookup"><span data-stu-id="20964-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="20964-119">**false**</span><span class="sxs-lookup"><span data-stu-id="20964-119">**false**</span></span>
  
- <span data-ttu-id="20964-120">Кэширование отключено.</span><span class="sxs-lookup"><span data-stu-id="20964-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20964-121">См. также</span><span class="sxs-lookup"><span data-stu-id="20964-121">See also</span></span>



[<span data-ttu-id="20964-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="20964-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

