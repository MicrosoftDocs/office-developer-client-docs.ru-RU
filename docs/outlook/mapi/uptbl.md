---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812591"
---
# <a name="uptbl"></a><span data-ttu-id="76077-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="76077-103">UPTBL</span></span>

<span data-ttu-id="76077-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76077-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76077-105">Информация для загрузки содержимого папки во время [загрузки состояния в таблице](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="76077-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76077-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="76077-106">Quick info</span></span>

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a><span data-ttu-id="76077-107">Members</span><span class="sxs-lookup"><span data-stu-id="76077-107">Members</span></span>

<span data-ttu-id="76077-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="76077-108">_ulFlags_</span></span>
  
> <span data-ttu-id="76077-109">[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="76077-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="76077-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="76077-110">UPT_OK</span></span>
    
    - <span data-ttu-id="76077-111">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="76077-111">[in] Upload was successful.</span></span> <span data-ttu-id="76077-112">Клиент устанавливает это после отправки контента папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="76077-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="76077-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="76077-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="76077-114">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76077-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="76077-115">_параметра pszName_</span><span class="sxs-lookup"><span data-stu-id="76077-115">_pszName_</span></span>
  
> <span data-ttu-id="76077-116">[out] Имя папки.</span><span class="sxs-lookup"><span data-stu-id="76077-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="76077-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="76077-117">_feid_</span></span>
  
> <span data-ttu-id="76077-118">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="76077-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="76077-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="76077-119">_uintReserved_</span></span>
  
> <span data-ttu-id="76077-120">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76077-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="76077-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="76077-121">_rgte_</span></span>
  
> <span data-ttu-id="76077-122">[out] Структура для хранения следующие сведения для обычного (или не скрыты) элементы и связанные (или скрытых) элементы в папке: _rgte [0]_ — для обычных элементов, а _rgte [1]_ — для связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="76077-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="76077-123">число новые или измененные элементы</span><span class="sxs-lookup"><span data-stu-id="76077-123">the number of new or modified items</span></span>
   - <span data-ttu-id="76077-124">число чтения элементов</span><span class="sxs-lookup"><span data-stu-id="76077-124">the number of read items</span></span> 
   - <span data-ttu-id="76077-125">Количество удаленных элементов</span><span class="sxs-lookup"><span data-stu-id="76077-125">the number of deleted items</span></span>
    
 <span data-ttu-id="76077-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="76077-126">_iEnt_</span></span>
  
> <span data-ttu-id="76077-127">[out] Индекс для отслеживания Отправка изменений, указанного идентификатором _централизованной_.</span><span class="sxs-lookup"><span data-stu-id="76077-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="76077-128">_централизованной_</span><span class="sxs-lookup"><span data-stu-id="76077-128">_cEnt_</span></span>
  
> <span data-ttu-id="76077-129">[out] Количество изменений в папку.</span><span class="sxs-lookup"><span data-stu-id="76077-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="76077-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="76077-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="76077-131">[out] Цепочка [UPMOV](upmov.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="76077-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="76077-132">_Сохраняются_</span><span class="sxs-lookup"><span data-stu-id="76077-132">_pReserved_</span></span>
  
> <span data-ttu-id="76077-133">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76077-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76077-134">См. также</span><span class="sxs-lookup"><span data-stu-id="76077-134">See also</span></span>

- [<span data-ttu-id="76077-135">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="76077-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="76077-136">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="76077-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="76077-137">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="76077-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="76077-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="76077-138">UPTBLE</span></span>](uptble.md)

