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
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391950"
---
# <a name="dntble"></a><span data-ttu-id="43b48-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="43b48-103">DNTBLE</span></span>

  
  
<span data-ttu-id="43b48-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43b48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43b48-105">Информация для загрузки содержимого папки с сервера во время [загрузки состояния в таблице](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="43b48-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="43b48-106">Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="43b48-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="43b48-107">Дополнительные сведения о ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="43b48-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="43b48-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="43b48-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="43b48-109">Members</span><span class="sxs-lookup"><span data-stu-id="43b48-109">Members</span></span>

 <span data-ttu-id="43b48-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="43b48-110">_cEntNew_</span></span>
  
> <span data-ttu-id="43b48-111">[out] Число элементов, добавленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="43b48-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="43b48-112">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="43b48-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="43b48-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="43b48-113">_cEntMod_</span></span>
  
> <span data-ttu-id="43b48-114">[out] Число элементов, измененных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="43b48-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="43b48-115">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="43b48-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="43b48-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="43b48-116">_cEntRead_</span></span>
  
> <span data-ttu-id="43b48-117">[out] Количество элементов чтения или помеченные непрочитанные сообщения для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="43b48-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="43b48-118">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="43b48-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="43b48-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="43b48-119">_cEntDel_</span></span>
  
> <span data-ttu-id="43b48-120">[out] Число элементов, удаленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="43b48-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="43b48-121">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="43b48-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43b48-122">См. также</span><span class="sxs-lookup"><span data-stu-id="43b48-122">See also</span></span>



[<span data-ttu-id="43b48-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="43b48-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="43b48-124">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="43b48-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="43b48-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="43b48-125">DNTBL</span></span>](dntbl.md)

