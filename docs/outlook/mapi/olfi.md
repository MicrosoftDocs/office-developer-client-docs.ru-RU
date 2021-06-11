---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279755"
---
# <a name="olfi"></a><span data-ttu-id="312ba-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="312ba-103">OLFI</span></span>

  
  
<span data-ttu-id="312ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="312ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="312ba-105">Очередь долгосрочных структур ID, используемых поставщиком файлов персональных папок (PST) для назначения ID входа для нового сообщения или папки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="312ba-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="312ba-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="312ba-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="312ba-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="312ba-107">Members</span></span>

 <span data-ttu-id="312ba-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="312ba-108">_ulVersion_</span></span>
  
- <span data-ttu-id="312ba-109">Номер версии для структуры.</span><span class="sxs-lookup"><span data-stu-id="312ba-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="312ba-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="312ba-110">_muidReserved_</span></span>
  
- <span data-ttu-id="312ba-111">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="312ba-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="312ba-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="312ba-112">_ulReserved_</span></span>
  
- <span data-ttu-id="312ba-113">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="312ba-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="312ba-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="312ba-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="312ba-115">Количество записей, доступных для выделения.</span><span class="sxs-lookup"><span data-stu-id="312ba-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="312ba-116">Эти записи имеют один и тот же глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="312ba-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="312ba-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="312ba-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="312ba-118">Количество записей, доступных далее для выделения.</span><span class="sxs-lookup"><span data-stu-id="312ba-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="312ba-119">Эти записи имеют один и тот же GUID.</span><span class="sxs-lookup"><span data-stu-id="312ba-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="312ba-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="312ba-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="312ba-121">Долгосрочная структура ID, **[LTID,](ltid.md)** идентифицирует запись, доступную в настоящее время для выделения.</span><span class="sxs-lookup"><span data-stu-id="312ba-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="312ba-122">Структура долгосрочного ID содержит GUID и индекс, идентифицирующий объект в магазине.</span><span class="sxs-lookup"><span data-stu-id="312ba-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="312ba-123">Вместе GUID и индекс могут сформировать уникальный ID входа для объекта.</span><span class="sxs-lookup"><span data-stu-id="312ba-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="312ba-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="312ba-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="312ba-125">Долгосрочная структура идентификации, определяемая следующей доступной записью.</span><span class="sxs-lookup"><span data-stu-id="312ba-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="312ba-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="312ba-126">Remarks</span></span>

<span data-ttu-id="312ba-127">Идентификатор входа — это идентификатор записи MAPI с 4-byte для папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="312ba-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="312ba-128">Дополнительные сведения см. в [записи ENTRYID.](https://msdn.microsoft.com/library/ms836424)</span><span class="sxs-lookup"><span data-stu-id="312ba-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="312ba-129">Когда поставщик PST-магазина назначает идентификатор входа новому объекту, сначала ему требуется GUID, идентифицирует сервер, и индекс, который идентифицирует объект в магазине.</span><span class="sxs-lookup"><span data-stu-id="312ba-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="312ba-130">Несмотря на то, что GUID не является уникальным для всех ID-записей, GUID и комбинированный индекс предоставляют уникальную запись.</span><span class="sxs-lookup"><span data-stu-id="312ba-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="312ba-131">Эта пара GUID и индекса отслеживается долгосрочной структурой **ID, LTID,** которая является частью **структуры OLFI.**</span><span class="sxs-lookup"><span data-stu-id="312ba-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="312ba-132">Поставщик магазинов PST физически не сохраняет в **OLFI** **структуру LTID** для каждой пары GUID-index.</span><span class="sxs-lookup"><span data-stu-id="312ba-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="312ba-133">Он сохраняет одну **структуру LTID,**  *ltidAlloc,*  для первой доступной в настоящее время пары GUID-index; количество,  *dwAlloc*  , из числа доступных записей, которые разделяют этот же GUID; и вторая **структура LTID,**  *ltidNextAlloc,*  для следующей доступной пары GUID-index, которая имеет другой GUID.</span><span class="sxs-lookup"><span data-stu-id="312ba-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="312ba-134">Поставщик магазина PST использует **структуру OLFI** для отслеживания переданных им GUID-интерфейсов и индексов. На виртуальном уровне поставщик сохраняет резерв нескольких структур **LTID,** которые готовы к выделению.</span><span class="sxs-lookup"><span data-stu-id="312ba-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="312ba-135">*dwAlloc* поддерживает количество доступных **структур LTID.**</span><span class="sxs-lookup"><span data-stu-id="312ba-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="312ba-136">Запросы на входные ИД приходят в блоки.</span><span class="sxs-lookup"><span data-stu-id="312ba-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="312ba-137">При запросе блокировки поставщик магазинов PST проверяет наличие достаточного резерва, сравнив запрашиваемого размера с *dwAlloc.*</span><span class="sxs-lookup"><span data-stu-id="312ba-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="312ba-138">Если резерва достаточно, он возвращает GUID и индекс в  *ltidAlloc*  для выделения.</span><span class="sxs-lookup"><span data-stu-id="312ba-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="312ba-139">Затем он уменьшает  *dwAlloc*  на запрашиваемом размере и прибавка индекса  *в ltidAlloc*  на запрашиваемом размере.</span><span class="sxs-lookup"><span data-stu-id="312ba-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="312ba-140">Это подготавливает поставщика магазинов PST к выделению  *ltidAlloc*  на следующий запрос для другого блока ID записи.</span><span class="sxs-lookup"><span data-stu-id="312ba-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="312ba-141">Обратите внимание, что GUID остается таким же для следующего запроса.</span><span class="sxs-lookup"><span data-stu-id="312ba-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="312ba-142">Если размер запроса больше, чем  *dwAlloc,*  поставщик магазинов PST пытается использовать то, что имеет следующий в резерве, как указано  *dwNextAlloc*  и  *ltidNextAlloc*  .</span><span class="sxs-lookup"><span data-stu-id="312ba-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="312ba-143">Он копирует  *dwNextAlloc*  и  *ltidNextAlloc*  соответственно  *dwAlloc*  и  *ltidAlloc*  и задает  *dwNextAlloc*  и  *ltidNextAlloc*  nULL.</span><span class="sxs-lookup"><span data-stu-id="312ba-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="312ba-144">Поставщик, который обертывал поставщика магазинов PST, должен периодически проверять  *ltidNextAlloc,*  чтобы узнать, является ли он NULL.</span><span class="sxs-lookup"><span data-stu-id="312ba-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="312ba-145">Если это так, поставщик должен заполнить его новым GUID и сбросить  *dwNextAlloc,*  чтобы можно было выделить дополнительные ID-записи.</span><span class="sxs-lookup"><span data-stu-id="312ba-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="312ba-146">См. также</span><span class="sxs-lookup"><span data-stu-id="312ba-146">See also</span></span>



[<span data-ttu-id="312ba-147">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="312ba-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="312ba-148">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="312ba-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="312ba-149">LTID</span><span class="sxs-lookup"><span data-stu-id="312ba-149">LTID</span></span>](ltid.md)

