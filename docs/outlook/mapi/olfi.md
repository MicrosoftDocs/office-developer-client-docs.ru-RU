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
# <a name="olfi"></a><span data-ttu-id="fc8ab-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="fc8ab-103">OLFI</span></span>

  
  
<span data-ttu-id="fc8ab-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc8ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc8ab-105">Очередь долгосрочных ИДЕНТИФИКАТОРов, используемых поставщиком хранилища файлов личных папок (PST) для назначения идентификатора записи для нового сообщения или папки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc8ab-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fc8ab-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="fc8ab-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="fc8ab-107">Members</span></span>

 <span data-ttu-id="fc8ab-108">_Улверсион_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-108">_ulVersion_</span></span>
  
- <span data-ttu-id="fc8ab-109">Номер версии структуры.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="fc8ab-110">_Муидресервед_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-110">_muidReserved_</span></span>
  
- <span data-ttu-id="fc8ab-111">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="fc8ab-112">_Улресервед_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-112">_ulReserved_</span></span>
  
- <span data-ttu-id="fc8ab-113">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="fc8ab-114">_Дваллок_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="fc8ab-115">Число записей, доступных для выделения.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="fc8ab-116">Эти записи используют один глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="fc8ab-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="fc8ab-117">_Двнексталлок_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="fc8ab-118">Число записей, доступных для размещения рядом.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="fc8ab-119">Эти записи используют один GUID.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="fc8ab-120">_Лтидаллок_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="fc8ab-121">Длинная структура ИДЕНТИФИКАТОРов **[лтид](ltid.md)**, определяющая запись, доступную в данный момент для выделения.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="fc8ab-122">Долгосрочная структура идентификатора содержит GUID и индекс, идентифицирующий объект в хранилище.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="fc8ab-123">Вместе идентификатор GUID и индекс могут иметь уникальный идентификатор записи для объекта.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="fc8ab-124">_Лтиднексталлок_</span><span class="sxs-lookup"><span data-stu-id="fc8ab-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="fc8ab-125">Длинная структура ИДЕНТИФИКАТОРов терминов, определяющая следующую доступную запись.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc8ab-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc8ab-126">Remarks</span></span>

<span data-ttu-id="fc8ab-127">Идентификатор записи — это 4-байтовый идентификатор записи MAPI для папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="fc8ab-128">Дополнительные сведения см. [](https://msdn.microsoft.com/library/ms836424)</span><span class="sxs-lookup"><span data-stu-id="fc8ab-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="fc8ab-129">Когда поставщик PST-хранилища назначает идентификатор записи новому объекту, ему сначала требуется идентификатор GUID, идентифицирующий сервер, и индекс, который определяет объект в хранилище.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="fc8ab-130">Несмотря на то, что идентификатор GUID не уникален для всех идентификаторов записей, GUID и комбинированный индекс предоставляют уникальную запись.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="fc8ab-131">Этот идентификатор GUID и эта комбинация индекса отслеживаются с помощью долгосрочной структуры ИДЕНТИФИКАТОРов, **лтид**, которая является частью структуры **олфи** .</span><span class="sxs-lookup"><span data-stu-id="fc8ab-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="fc8ab-132">Поставщик хранилища PST не сохраняет **олфи** структуру **лтид** для каждой из этих комбинаций GUID-index.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="fc8ab-133">Он сохраняет одну структуру **лтид** , *лтидаллок* для первой доступной в текущий момент связывания GUID и индекса; число, *дваллок* , количество доступных записей, которые совместно используют этот GUID; Вторая структура **лтид** , *лтиднексталлок* для следующего доступного ключа GUID-index с другим GUID.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="fc8ab-134">Поставщик PST-хранилища использует структуру **олфи** для отслеживания идентификаторов GUID и индексов, которые он передают. На виртуальном уровне поставщик поддерживает резервное число структур **лтид** , готовых к выделению.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="fc8ab-135">*дваллок* поддерживает количество доступных структур **лтид** .</span><span class="sxs-lookup"><span data-stu-id="fc8ab-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="fc8ab-136">Запросы для идентификаторов записей поступают в блоки.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="fc8ab-137">При наличии запроса на блокировку поставщик хранилища PST проверяет, достаточно ли резерва, сравнив запрошенный размер с *дваллок* .</span><span class="sxs-lookup"><span data-stu-id="fc8ab-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="fc8ab-138">При наличии достаточного резервирования он возвращает GUID и индекс в *лтидаллок* для выделения.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="fc8ab-139">Затем он уменьшает *дваллок* по запрошенному размеру и увеличивает индекс в *лтидаллок* на запрошенный размер.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="fc8ab-140">При этом поставщик хранилища PST подготавливается к выделению *лтидаллок* при следующем запросе для другого блока идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="fc8ab-141">Обратите внимание, что GUID для следующего запроса остается прежним.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="fc8ab-142">Если размер запроса превышает *дваллок* , поставщик PST-хранилища пытается использовать его в резервировании, как указано в *двнексталлок* и *лтиднексталлок* .</span><span class="sxs-lookup"><span data-stu-id="fc8ab-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="fc8ab-143">Он копирует *двнексталлок* и *лтиднексталлок* в *дваллок* и *Лтидаллок* , СООТВЕТСТВЕННО, и задает для *двнексталлок* и *лтиднексталлок* значение null.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="fc8ab-144">Поставщик, который включает в себя оболочку поставщика хранилища PST, должен периодически проверять *лтиднексталлок* , чтобы проверить, имеет ли он значение null.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="fc8ab-145">Если это так, поставщик должен заполнить его новым GUID и сбросить *двнексталлок* , чтобы можно было выделить дополнительные идентификаторы записи.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc8ab-146">См. также</span><span class="sxs-lookup"><span data-stu-id="fc8ab-146">See also</span></span>



[<span data-ttu-id="fc8ab-147">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="fc8ab-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="fc8ab-148">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="fc8ab-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="fc8ab-149">LTID</span><span class="sxs-lookup"><span data-stu-id="fc8ab-149">LTID</span></span>](ltid.md)

