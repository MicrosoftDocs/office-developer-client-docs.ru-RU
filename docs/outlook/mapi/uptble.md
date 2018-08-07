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
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812577"
---
# <a name="uptble"></a><span data-ttu-id="61579-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="61579-103">UPTBLE</span></span>

<span data-ttu-id="61579-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61579-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61579-105">Подробные данные для загрузки содержимого папки во время [загрузки состояния в таблице](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="61579-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61579-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="61579-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="61579-107">Members</span><span class="sxs-lookup"><span data-stu-id="61579-107">Members</span></span>

 <span data-ttu-id="61579-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="61579-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="61579-109">[out] Индекс для отслеживания отправки _cEntMod_ число новые или измененные элементы.</span><span class="sxs-lookup"><span data-stu-id="61579-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="61579-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="61579-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="61579-111">[out] Число новые или измененные элементы в папке.</span><span class="sxs-lookup"><span data-stu-id="61579-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="61579-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="61579-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="61579-113">[out] Индексирование для отслеживания Отправка число _cEntRead_ чтение элементов.</span><span class="sxs-lookup"><span data-stu-id="61579-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="61579-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="61579-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="61579-115">[out] Количество чтения элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="61579-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="61579-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="61579-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="61579-117">[out] Индекс для отслеживания Отправка число _cEntDel_ удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="61579-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="61579-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="61579-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="61579-119">[out] Количество удаленных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="61579-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="61579-120">См. также</span><span class="sxs-lookup"><span data-stu-id="61579-120">See also</span></span>

- [<span data-ttu-id="61579-121">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="61579-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="61579-122">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="61579-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="61579-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="61579-123">UPTBL</span></span>](uptbl.md)

