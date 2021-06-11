---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413842"
---
# <a name="uptble"></a><span data-ttu-id="d4346-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="d4346-103">UPTBLE</span></span>

<span data-ttu-id="d4346-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4346-105">Расширенные сведения для загрузки содержимого папки во время [состояния таблицы отправки.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="d4346-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d4346-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d4346-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="d4346-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d4346-107">Members</span></span>

 <span data-ttu-id="d4346-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="d4346-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="d4346-109">[вышел] Индекс для отслеживания загрузки  _номера cEntMod_ новых или измененных элементов.</span><span class="sxs-lookup"><span data-stu-id="d4346-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="d4346-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="d4346-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="d4346-111">[вышел] Количество новых или измененных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="d4346-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="d4346-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="d4346-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="d4346-113">[вышел] Индекс для отслеживания загрузки количества элементов _чтения cEntRead._</span><span class="sxs-lookup"><span data-stu-id="d4346-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="d4346-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="d4346-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="d4346-115">[вышел] Количество элементов чтения в папке.</span><span class="sxs-lookup"><span data-stu-id="d4346-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="d4346-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="d4346-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="d4346-117">[вышел] Индекс для отслеживания загрузки количества _удаленных элементов cEntDel._</span><span class="sxs-lookup"><span data-stu-id="d4346-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="d4346-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="d4346-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="d4346-119">[вышел] Количество удаленных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="d4346-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d4346-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d4346-120">See also</span></span>

- [<span data-ttu-id="d4346-121">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="d4346-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="d4346-122">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="d4346-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d4346-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="d4346-123">UPTBL</span></span>](uptbl.md)

