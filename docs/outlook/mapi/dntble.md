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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337116"
---
# <a name="dntble"></a><span data-ttu-id="21003-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="21003-103">DNTBLE</span></span>

  
  
<span data-ttu-id="21003-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21003-105">Информация для скачивания содержимого папки с сервера при [загрузке таблицы состояние](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="21003-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="21003-106">Процесс скачивания использует синхронизацию добавочных изменений (ICS) Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="21003-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="21003-107">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="21003-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="21003-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="21003-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="21003-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="21003-109">Members</span></span>

 <span data-ttu-id="21003-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="21003-110">_cEntNew_</span></span>
  
> <span data-ttu-id="21003-111">[out] Количество элементов, добавленных в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="21003-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="21003-112">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="21003-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="21003-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="21003-113">_cEntMod_</span></span>
  
> <span data-ttu-id="21003-114">[out] Количество элементов, измененных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="21003-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="21003-115">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="21003-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="21003-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="21003-116">_cEntRead_</span></span>
  
> <span data-ttu-id="21003-117">[out] Количество элементов, прочитанных или помеченных как непрочитанные в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="21003-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="21003-118">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="21003-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="21003-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="21003-119">_cEntDel_</span></span>
  
> <span data-ttu-id="21003-120">[out] Количество элементов, удаленных из локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="21003-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="21003-121">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="21003-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21003-122">См. также</span><span class="sxs-lookup"><span data-stu-id="21003-122">See also</span></span>



[<span data-ttu-id="21003-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="21003-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="21003-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="21003-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="21003-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="21003-125">DNTBL</span></span>](dntbl.md)

