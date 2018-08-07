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
ms.openlocfilehash: 82923895353cf600c4d0b78b9a6e16fc7d57e466
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812435"
---
# <a name="synccont"></a><span data-ttu-id="8e054-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="8e054-103">SYNCCONT</span></span>

<span data-ttu-id="8e054-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e054-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e054-105">Сведения о синхронизации содержимое указанных папках в локальном хранилище с сервером во время [синхронизации состояние содержимого](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="8e054-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="8e054-106">Это включает в себя только что отправку пользователями или полную синхронизацию, передаваемых и выберите файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="8e054-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8e054-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8e054-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8e054-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e054-108">Members</span></span>

<span data-ttu-id="8e054-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e054-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8e054-110">[in] Флаги для определения соответствующего поведения при синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8e054-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="8e054-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="8e054-111">UPC_OK</span></span>
    
  - <span data-ttu-id="8e054-112">[in] Отправка или полная синхронизация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="8e054-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="8e054-113">Клиент устанавливает это после синхронизация данных с сервером.</span><span class="sxs-lookup"><span data-stu-id="8e054-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="8e054-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="8e054-114">_iEnt_</span></span>
  
> <span data-ttu-id="8e054-115">[out] Индекс для отслеживания синхронизацию содержимого в поле число папок, указанного идентификатором _централизованной_.</span><span class="sxs-lookup"><span data-stu-id="8e054-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="8e054-116">_централизованной_</span><span class="sxs-lookup"><span data-stu-id="8e054-116">_cEnt_</span></span>
  
> <span data-ttu-id="8e054-117">[out] Число папок, которые следует реплицировать.</span><span class="sxs-lookup"><span data-stu-id="8e054-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="8e054-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="8e054-118">_pvReserved_</span></span>
  
> <span data-ttu-id="8e054-119">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e054-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8e054-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="8e054-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="8e054-121">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e054-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8e054-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="8e054-122">_psosReserved_</span></span>
  
> <span data-ttu-id="8e054-123">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e054-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8e054-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8e054-124">See also</span></span>

- [<span data-ttu-id="8e054-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="8e054-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="8e054-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="8e054-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="8e054-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="8e054-127">MAPI Constants</span></span>](mapi-constants.md)

