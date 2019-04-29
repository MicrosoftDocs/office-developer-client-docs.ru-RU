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
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438115"
---
# <a name="uptbl"></a><span data-ttu-id="2c57a-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="2c57a-103">UPTBL</span></span>

<span data-ttu-id="2c57a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c57a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c57a-105">Сведения для отправки содержимого папки во время [состояния таблицы отправки](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="2c57a-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2c57a-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="2c57a-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="2c57a-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2c57a-107">Members</span></span>

<span data-ttu-id="2c57a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c57a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="2c57a-109">возврата Флаги, необходимые для определения поведения при отправке.</span><span class="sxs-lookup"><span data-stu-id="2c57a-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="2c57a-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="2c57a-110">UPT_OK</span></span>
    
    - <span data-ttu-id="2c57a-111">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2c57a-111">[in] Upload was successful.</span></span> <span data-ttu-id="2c57a-112">Клиент устанавливает это после отправки содержимого папки на сервер.</span><span class="sxs-lookup"><span data-stu-id="2c57a-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="2c57a-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="2c57a-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="2c57a-114">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c57a-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="2c57a-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="2c57a-115">_pszName_</span></span>
  
> <span data-ttu-id="2c57a-116">[out] Имя папки.</span><span class="sxs-lookup"><span data-stu-id="2c57a-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="2c57a-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="2c57a-117">_feid_</span></span>
  
> <span data-ttu-id="2c57a-118">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="2c57a-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="2c57a-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="2c57a-119">_uintReserved_</span></span>
  
> <span data-ttu-id="2c57a-120">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c57a-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="2c57a-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="2c57a-121">_rgte_</span></span>
  
> <span data-ttu-id="2c57a-122">вышли Структура для хранения следующих данных для обычных (или не скрытых) элементов и связанных (или скрытых) элементов в папке: _rgte [0]_ для обычных элементов, а _rgte [1]_ — для связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="2c57a-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="2c57a-123">число новых или измененных элементов</span><span class="sxs-lookup"><span data-stu-id="2c57a-123">the number of new or modified items</span></span>
   - <span data-ttu-id="2c57a-124">количество прочитанных элементов</span><span class="sxs-lookup"><span data-stu-id="2c57a-124">the number of read items</span></span> 
   - <span data-ttu-id="2c57a-125">число удаленных элементов</span><span class="sxs-lookup"><span data-stu-id="2c57a-125">the number of deleted items</span></span>
    
 <span data-ttu-id="2c57a-126">_Иент_</span><span class="sxs-lookup"><span data-stu-id="2c57a-126">_iEnt_</span></span>
  
> <span data-ttu-id="2c57a-127">вышли Индекс для отслеживания количества изменений, заданных с помощью цента __.</span><span class="sxs-lookup"><span data-stu-id="2c57a-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="2c57a-128">_Центов_</span><span class="sxs-lookup"><span data-stu-id="2c57a-128">_cEnt_</span></span>
  
> <span data-ttu-id="2c57a-129">вышли Количество изменений в папке.</span><span class="sxs-lookup"><span data-stu-id="2c57a-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="2c57a-130">_Пупмовхеад_</span><span class="sxs-lookup"><span data-stu-id="2c57a-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="2c57a-131">вышли Цепочка структур [упмов](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="2c57a-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="2c57a-132">_Сохранен_</span><span class="sxs-lookup"><span data-stu-id="2c57a-132">_pReserved_</span></span>
  
> <span data-ttu-id="2c57a-133">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2c57a-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c57a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2c57a-134">See also</span></span>

- [<span data-ttu-id="2c57a-135">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="2c57a-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="2c57a-136">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="2c57a-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="2c57a-137">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="2c57a-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="2c57a-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="2c57a-138">UPTBLE</span></span>](uptble.md)

