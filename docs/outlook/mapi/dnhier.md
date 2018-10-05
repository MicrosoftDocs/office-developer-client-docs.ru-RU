---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389087"
---
# <a name="dnhier"></a><span data-ttu-id="22618-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="22618-103">DNHIER</span></span>

<span data-ttu-id="22618-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22618-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22618-105">Сведения для загрузки иерархии с сервера во время, [Загрузите иерархия состояний](download-hierarchy-state.md), которая является частью полную иерархию синхронизации.</span><span class="sxs-lookup"><span data-stu-id="22618-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="22618-106">Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="22618-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="22618-107">Дополнительные сведения о ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="22618-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="22618-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="22618-108">Quick info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="22618-109">Members</span><span class="sxs-lookup"><span data-stu-id="22618-109">Members</span></span>

<span data-ttu-id="22618-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22618-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="22618-111">[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="22618-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="22618-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="22618-112">DNH_OK</span></span>
    
   - <span data-ttu-id="22618-113">[in] Загрузка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="22618-113">[in] Download was successful.</span></span> <span data-ttu-id="22618-114">Клиент устанавливает это после загрузки информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="22618-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="22618-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="22618-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="22618-116">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="22618-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="22618-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="22618-117">_pxihc_</span></span>
  
>  <span data-ttu-id="22618-118">[out] Указатель на интерфейс **IExchangeImportHierarchyChanges** иерархии, которая поддерживает загрузки изменений добавочного иерархии.</span><span class="sxs-lookup"><span data-stu-id="22618-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="22618-119">Дополнительные сведения о **IExchangeImportHierarchyChanges** [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="22618-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="22618-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="22618-120">_cEntNew_</span></span>
  
> <span data-ttu-id="22618-121">[out] Число папки, добавленные в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="22618-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="22618-122">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="22618-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="22618-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="22618-123">_cEntMod_</span></span>
  
> <span data-ttu-id="22618-124">[out] Число папок, которые следует изменить для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="22618-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="22618-125">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="22618-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="22618-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="22618-126">_cEntDel_</span></span>
  
> <span data-ttu-id="22618-127">[out] Число папок к удалению локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="22618-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="22618-128">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="22618-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22618-129">См. также</span><span class="sxs-lookup"><span data-stu-id="22618-129">See also</span></span>

- [<span data-ttu-id="22618-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="22618-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="22618-131">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="22618-131">MAPI Constants</span></span>](mapi-constants.md)

