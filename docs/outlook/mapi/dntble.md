---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: d92e8d7b3fb14051ffceb829f3df3f6fa12e6e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565860"
---
# <a name="dntble"></a><span data-ttu-id="f3254-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="f3254-103">DNTBLE</span></span>

  
  
<span data-ttu-id="f3254-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3254-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3254-105">Информация для загрузки содержимого папки с сервера во время [загрузки состояния в таблице](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="f3254-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="f3254-106">Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="f3254-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="f3254-107">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="f3254-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f3254-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f3254-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="f3254-109">Members</span><span class="sxs-lookup"><span data-stu-id="f3254-109">Members</span></span>

 <span data-ttu-id="f3254-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="f3254-110">_cEntNew_</span></span>
  
> <span data-ttu-id="f3254-111">[out] Число элементов, добавленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="f3254-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="f3254-112">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="f3254-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="f3254-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="f3254-113">_cEntMod_</span></span>
  
> <span data-ttu-id="f3254-114">[out] Число элементов, измененных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="f3254-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="f3254-115">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="f3254-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="f3254-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="f3254-116">_cEntRead_</span></span>
  
> <span data-ttu-id="f3254-117">[out] Количество элементов чтения или помеченные непрочитанные сообщения для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="f3254-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="f3254-118">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="f3254-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="f3254-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="f3254-119">_cEntDel_</span></span>
  
> <span data-ttu-id="f3254-120">[out] Число элементов, удаленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="f3254-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="f3254-121">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="f3254-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3254-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f3254-122">See also</span></span>



[<span data-ttu-id="f3254-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="f3254-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f3254-124">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="f3254-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f3254-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="f3254-125">DNTBL</span></span>](dntbl.md)

