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
# <a name="uptble"></a><span data-ttu-id="983e2-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="983e2-103">UPTBLE</span></span>

<span data-ttu-id="983e2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="983e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="983e2-105">Расширенные сведения для отправки содержимого папки во время [состояния таблицы отправки](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="983e2-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="983e2-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="983e2-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="983e2-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="983e2-107">Members</span></span>

 <span data-ttu-id="983e2-108">_иентмод_</span><span class="sxs-lookup"><span data-stu-id="983e2-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="983e2-109">вышли Индекс для отслеживания отправки _центмод_ числа новых или измененных элементов.</span><span class="sxs-lookup"><span data-stu-id="983e2-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="983e2-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="983e2-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="983e2-111">вышли Количество новых или измененных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="983e2-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="983e2-112">_иентреад_</span><span class="sxs-lookup"><span data-stu-id="983e2-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="983e2-113">вышли Индекс для отслеживания отгрузки числа прочитанных элементов _центреад_ .</span><span class="sxs-lookup"><span data-stu-id="983e2-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="983e2-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="983e2-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="983e2-115">вышли Количество прочитанных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="983e2-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="983e2-116">_иентдел_</span><span class="sxs-lookup"><span data-stu-id="983e2-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="983e2-117">вышли Индекс для отслеживания отправки числа удаленных элементов _центдел_ .</span><span class="sxs-lookup"><span data-stu-id="983e2-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="983e2-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="983e2-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="983e2-119">вышли Количество удаленных элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="983e2-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="983e2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="983e2-120">See also</span></span>

- [<span data-ttu-id="983e2-121">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="983e2-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="983e2-122">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="983e2-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="983e2-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="983e2-123">UPTBL</span></span>](uptbl.md)

