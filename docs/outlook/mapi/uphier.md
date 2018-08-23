---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592096"
---
# <a name="uphier"></a><span data-ttu-id="a527d-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="a527d-103">UPHIER</span></span>
 
<span data-ttu-id="a527d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a527d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a527d-105">Сведения о синхронизации иерархии папок во время [загрузки иерархия состояний](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="a527d-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a527d-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a527d-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="a527d-107">Members</span><span class="sxs-lookup"><span data-stu-id="a527d-107">Members</span></span>

<span data-ttu-id="a527d-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a527d-108">_ulFlags_</span></span>
  
> <span data-ttu-id="a527d-109">[in] Флаги для изменения поведения при синхронизации иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="a527d-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="a527d-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="a527d-110">UPH_OK</span></span>
    
    - <span data-ttu-id="a527d-111">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="a527d-111">[in] Upload was successful.</span></span> <span data-ttu-id="a527d-112">Клиент устанавливает это после успешной отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="a527d-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="a527d-113">После просмотра этот флаг, Outlook удаляет все сведения о внутренней регистрации, который сообщил, что требуется обновление иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="a527d-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="a527d-114">Клиент передает значение HRESULT, если передача не удалась.</span><span class="sxs-lookup"><span data-stu-id="a527d-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="a527d-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="a527d-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="a527d-116">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a527d-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="a527d-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="a527d-117">_iEnt_</span></span>
  
> <span data-ttu-id="a527d-118">[out] Индекс для отслеживания синхронизация число папок, указанного идентификатором *централизованной* .</span><span class="sxs-lookup"><span data-stu-id="a527d-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="a527d-119">_централизованной_</span><span class="sxs-lookup"><span data-stu-id="a527d-119">_cEnt_</span></span>
  
> <span data-ttu-id="a527d-120">[out] Число папок, которые не синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="a527d-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a527d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a527d-121">See also</span></span>

- [<span data-ttu-id="a527d-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="a527d-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="a527d-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="a527d-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a527d-124">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="a527d-124">MAPI Constants</span></span>](mapi-constants.md)

