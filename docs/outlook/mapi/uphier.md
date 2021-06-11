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
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414923"
---
# <a name="uphier"></a><span data-ttu-id="b1920-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="b1920-103">UPHIER</span></span>
 
<span data-ttu-id="b1920-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1920-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1920-105">Сведения для синхронизации иерархии папок во время [состояния иерархии загрузки.](upload-hierarchy-state.md)</span><span class="sxs-lookup"><span data-stu-id="b1920-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b1920-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b1920-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="b1920-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="b1920-107">Members</span></span>

<span data-ttu-id="b1920-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1920-108">_ulFlags_</span></span>
  
> <span data-ttu-id="b1920-109">[in] Флаги для изменения поведения при синхронизации иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="b1920-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="b1920-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="b1920-110">UPH_OK</span></span>
    
    - <span data-ttu-id="b1920-111">[in] Upload успешно.</span><span class="sxs-lookup"><span data-stu-id="b1920-111">[in] Upload was successful.</span></span> <span data-ttu-id="b1920-112">Клиент задает это после успешной загрузки данных на сервер.</span><span class="sxs-lookup"><span data-stu-id="b1920-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="b1920-113">При виде этого флага Outlook все внутренние сведения бухгалтерии, которые указывали на необходимость обновления иерархии папок.</span><span class="sxs-lookup"><span data-stu-id="b1920-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="b1920-114">Клиент передает HRESULT, если загрузка не была успешной.</span><span class="sxs-lookup"><span data-stu-id="b1920-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="b1920-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="b1920-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="b1920-116">[вышел] Этот член зарезервирован для Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b1920-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="b1920-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="b1920-117">_iEnt_</span></span>
  
> <span data-ttu-id="b1920-118">[вышел] Индекс для отслеживания синхронизации количества папок, указанных *cEnt.*</span><span class="sxs-lookup"><span data-stu-id="b1920-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="b1920-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="b1920-119">_cEnt_</span></span>
  
> <span data-ttu-id="b1920-120">[вышел] Количество не синхронизированных папок.</span><span class="sxs-lookup"><span data-stu-id="b1920-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1920-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b1920-121">See also</span></span>

- [<span data-ttu-id="b1920-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="b1920-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b1920-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="b1920-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b1920-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b1920-124">MAPI Constants</span></span>](mapi-constants.md)

