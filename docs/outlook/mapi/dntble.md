---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391950"
---
# <a name="dntble"></a><span data-ttu-id="99bfa-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="99bfa-103">DNTBLE</span></span>

  
  
<span data-ttu-id="99bfa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99bfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99bfa-105">Информация для скачивания содержимого папки с сервера при [загрузке таблицы состояние](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="99bfa-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="99bfa-106">Процесс скачивания использует синхронизацию добавочных изменений (ICS) Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="99bfa-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="99bfa-107">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="99bfa-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="99bfa-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="99bfa-108">Quick Info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="99bfa-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="99bfa-109">Members</span></span>

 <span data-ttu-id="99bfa-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="99bfa-110">_cEntNew_</span></span>
  
> <span data-ttu-id="99bfa-111">[] Количество элементов, добавленных в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="99bfa-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="99bfa-112">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="99bfa-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="99bfa-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="99bfa-113">_cEntMod_</span></span>
  
> <span data-ttu-id="99bfa-114">[] Количество элементов, измененных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="99bfa-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="99bfa-115">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="99bfa-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="99bfa-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="99bfa-116">_cEntRead_</span></span>
  
> <span data-ttu-id="99bfa-117">[] Количество элементов, прочитанных или помеченных как непрочитанные в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="99bfa-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="99bfa-118">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="99bfa-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="99bfa-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="99bfa-119">_cEntDel_</span></span>
  
> <span data-ttu-id="99bfa-120">[] Количество элементов, удаленных из локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="99bfa-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="99bfa-121">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="99bfa-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99bfa-122">См. также</span><span class="sxs-lookup"><span data-stu-id="99bfa-122">See also</span></span>



[<span data-ttu-id="99bfa-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="99bfa-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="99bfa-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="99bfa-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="99bfa-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="99bfa-125">DNTBL</span></span>](dntbl.md)

