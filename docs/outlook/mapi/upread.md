---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419886"
---
# <a name="upread"></a><span data-ttu-id="76620-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="76620-103">UPREAD</span></span>

  
  
<span data-ttu-id="76620-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76620-105">Сведения о загрузке состояния чтения элементов во время [отправки состояния чтения.](upload-read-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="76620-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76620-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="76620-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="76620-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="76620-107">Members</span></span>

 <span data-ttu-id="76620-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="76620-108">_pupre_</span></span>
  
>  <span data-ttu-id="76620-109">[out] Вектор **[записей UPREADE.](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="76620-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="76620-110">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="76620-110">_cEnt_</span></span>
  
>  <span data-ttu-id="76620-111">[out] Количество **записей UPREADE.**</span><span class="sxs-lookup"><span data-stu-id="76620-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="76620-112">См. также</span><span class="sxs-lookup"><span data-stu-id="76620-112">See also</span></span>



[<span data-ttu-id="76620-113">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="76620-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="76620-114">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="76620-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="76620-115">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="76620-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="76620-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="76620-116">UPREADE</span></span>](upreade.md)

