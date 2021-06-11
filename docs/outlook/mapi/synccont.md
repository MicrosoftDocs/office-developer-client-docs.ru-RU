---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430408"
---
# <a name="synccont"></a><span data-ttu-id="fb294-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="fb294-103">SYNCCONT</span></span>

<span data-ttu-id="fb294-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb294-105">Сведения для синхронизации содержимого указанных папок в локальном магазине с сервером во время состояния [синхронизации содержимого.](synchronize-contents-state.md)</span><span class="sxs-lookup"><span data-stu-id="fb294-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="fb294-106">Это включает только загрузку или полную синхронизацию с загрузкой, а затем скачиванием.</span><span class="sxs-lookup"><span data-stu-id="fb294-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fb294-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fb294-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="fb294-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="fb294-108">Members</span></span>

<span data-ttu-id="fb294-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fb294-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fb294-110">[in] Флаги для определения соответствующего поведения во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="fb294-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="fb294-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="fb294-111">UPC_OK</span></span>
    
  - <span data-ttu-id="fb294-112">[in] Upload или полная синхронизация была успешной.</span><span class="sxs-lookup"><span data-stu-id="fb294-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="fb294-113">Клиент задает это после синхронизации сведений с сервером.</span><span class="sxs-lookup"><span data-stu-id="fb294-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="fb294-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="fb294-114">_iEnt_</span></span>
  
> <span data-ttu-id="fb294-115">[вышел] Индекс для отслеживания синхронизации содержимого в количестве папок, указанных _cEnt._</span><span class="sxs-lookup"><span data-stu-id="fb294-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="fb294-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="fb294-116">_cEnt_</span></span>
  
> <span data-ttu-id="fb294-117">[вышел] Количество папок, которые необходимо реплицировать.</span><span class="sxs-lookup"><span data-stu-id="fb294-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="fb294-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="fb294-118">_pvReserved_</span></span>
  
> <span data-ttu-id="fb294-119">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fb294-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="fb294-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="fb294-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="fb294-121">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fb294-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="fb294-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="fb294-122">_psosReserved_</span></span>
  
> <span data-ttu-id="fb294-123">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fb294-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fb294-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fb294-124">See also</span></span>

- [<span data-ttu-id="fb294-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="fb294-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="fb294-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="fb294-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="fb294-127">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="fb294-127">MAPI Constants</span></span>](mapi-constants.md)

