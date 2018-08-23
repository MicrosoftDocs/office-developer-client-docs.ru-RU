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
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592341"
---
# <a name="uptble"></a><span data-ttu-id="a01b5-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="a01b5-103">UPTBLE</span></span>

<span data-ttu-id="a01b5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a01b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a01b5-105">Подробные данные для загрузки содержимого папки во время [загрузки состояния в таблице](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="a01b5-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a01b5-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a01b5-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a01b5-107">Members</span><span class="sxs-lookup"><span data-stu-id="a01b5-107">Members</span></span>

 <span data-ttu-id="a01b5-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="a01b5-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="a01b5-109">[out] Индекс для отслеживания отправки _cEntMod_ число новые или измененные элементы.</span><span class="sxs-lookup"><span data-stu-id="a01b5-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="a01b5-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="a01b5-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="a01b5-111">[out] Число новые или измененные элементы в папке.</span><span class="sxs-lookup"><span data-stu-id="a01b5-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="a01b5-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="a01b5-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="a01b5-113">[out] Индексирование для отслеживания Отправка число _cEntRead_ чтение элементов.</span><span class="sxs-lookup"><span data-stu-id="a01b5-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="a01b5-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="a01b5-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="a01b5-115">[out] Количество чтения элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="a01b5-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="a01b5-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="a01b5-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="a01b5-117">[out] Индекс для отслеживания Отправка число _cEntDel_ удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="a01b5-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="a01b5-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="a01b5-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="a01b5-119">[out] Количество удаленных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="a01b5-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a01b5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a01b5-120">See also</span></span>

- [<span data-ttu-id="a01b5-121">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="a01b5-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="a01b5-122">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="a01b5-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a01b5-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="a01b5-123">UPTBL</span></span>](uptbl.md)

