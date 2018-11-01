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
ms.openlocfilehash: bdfabdf02fc0fa6222418bd0fb87e9b6c17d936a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580441"
---
# <a name="uptbl"></a><span data-ttu-id="88c79-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="88c79-103">UPTBL</span></span>

<span data-ttu-id="88c79-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88c79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88c79-105">Информация для загрузки содержимого папки во время [загрузки состояния в таблице](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="88c79-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="88c79-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="88c79-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="88c79-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="88c79-107">Members</span></span>

<span data-ttu-id="88c79-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="88c79-108">_ulFlags_</span></span>
  
> <span data-ttu-id="88c79-109">[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="88c79-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="88c79-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="88c79-110">UPT_OK</span></span>
    
    - <span data-ttu-id="88c79-111">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="88c79-111">[in] Upload was successful.</span></span> <span data-ttu-id="88c79-112">Клиент устанавливает это после отправки контента папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="88c79-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="88c79-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="88c79-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="88c79-114">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="88c79-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="88c79-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="88c79-115">_pszName_</span></span>
  
> <span data-ttu-id="88c79-116">[out] Имя папки.</span><span class="sxs-lookup"><span data-stu-id="88c79-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="88c79-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="88c79-117">_feid_</span></span>
  
> <span data-ttu-id="88c79-118">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="88c79-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="88c79-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="88c79-119">_uintReserved_</span></span>
  
> <span data-ttu-id="88c79-120">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="88c79-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="88c79-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="88c79-121">_rgte_</span></span>
  
> <span data-ttu-id="88c79-122">[out] Структура для хранения следующие сведения для обычного (или не скрыты) элементы и связанные (или скрытых) элементы в папке: _rgte [0]_ — для обычных элементов, а _rgte [1]_ — для связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="88c79-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="88c79-123">число новые или измененные элементы</span><span class="sxs-lookup"><span data-stu-id="88c79-123">the number of new or modified items</span></span>
   - <span data-ttu-id="88c79-124">число чтения элементов</span><span class="sxs-lookup"><span data-stu-id="88c79-124">the number of read items</span></span> 
   - <span data-ttu-id="88c79-125">Количество удаленных элементов</span><span class="sxs-lookup"><span data-stu-id="88c79-125">the number of deleted items</span></span>
    
 <span data-ttu-id="88c79-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="88c79-126">_iEnt_</span></span>
  
> <span data-ttu-id="88c79-127">[out] Индекс для отслеживания Отправка изменений, указанного идентификатором _централизованной_.</span><span class="sxs-lookup"><span data-stu-id="88c79-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="88c79-128">_централизованной_</span><span class="sxs-lookup"><span data-stu-id="88c79-128">_cEnt_</span></span>
  
> <span data-ttu-id="88c79-129">[out] Количество изменений в папку.</span><span class="sxs-lookup"><span data-stu-id="88c79-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="88c79-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="88c79-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="88c79-131">[out] Цепочка [UPMOV](upmov.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="88c79-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="88c79-132">_Сохраняются_</span><span class="sxs-lookup"><span data-stu-id="88c79-132">_pReserved_</span></span>
  
> <span data-ttu-id="88c79-133">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="88c79-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88c79-134">См. также</span><span class="sxs-lookup"><span data-stu-id="88c79-134">See also</span></span>

- [<span data-ttu-id="88c79-135">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="88c79-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="88c79-136">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="88c79-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="88c79-137">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="88c79-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="88c79-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="88c79-138">UPTBLE</span></span>](uptble.md)

