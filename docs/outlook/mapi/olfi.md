---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ff23472254df2bd9d2195c7cf2c4258b856ec430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810056"
---
# <a name="olfi"></a><span data-ttu-id="e58d9-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="e58d9-103">OLFI</span></span>

  
  
<span data-ttu-id="e58d9-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e58d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e58d9-105">Очереди долгосрочного структур идентификатор используется файл личных папок (PST) поставщика хранилища для присваивается идентификатор записи для нового сообщения или папки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e58d9-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e58d9-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e58d9-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e58d9-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="e58d9-107">Members</span></span>

 <span data-ttu-id="e58d9-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="e58d9-108">_ulVersion_</span></span>
  
- <span data-ttu-id="e58d9-109">Номер версии для структуры.</span><span class="sxs-lookup"><span data-stu-id="e58d9-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="e58d9-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="e58d9-110">_muidReserved_</span></span>
  
- <span data-ttu-id="e58d9-111">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e58d9-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="e58d9-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="e58d9-112">_ulReserved_</span></span>
  
- <span data-ttu-id="e58d9-113">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e58d9-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="e58d9-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="e58d9-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="e58d9-115">Число записей, которые доступны для выделения.</span><span class="sxs-lookup"><span data-stu-id="e58d9-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="e58d9-116">Эти записи совместно использовать же глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="e58d9-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="e58d9-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="e58d9-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="e58d9-118">Число записей, которые доступны в Далее для выделения.</span><span class="sxs-lookup"><span data-stu-id="e58d9-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="e58d9-119">Эти записи имеют одинаковый идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="e58d9-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="e58d9-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="e58d9-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="e58d9-121">Долгосрочные идентификатор структуры, **[LTID](ltid.md)**, идентифицирующий запись в настоящее время недоступен для выделения.</span><span class="sxs-lookup"><span data-stu-id="e58d9-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="e58d9-122">Долгосрочные структура идентификатор содержит идентификатор GUID и индекса, идентифицирующий объекта в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e58d9-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="e58d9-123">Совместная работа GUID и индекса можно было создавать уникальный идентификатор записи для объекта.</span><span class="sxs-lookup"><span data-stu-id="e58d9-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="e58d9-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="e58d9-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="e58d9-125">Определение следующего доступные записи долгосрочного структура идентификатора.</span><span class="sxs-lookup"><span data-stu-id="e58d9-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e58d9-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="e58d9-126">Remarks</span></span>

<span data-ttu-id="e58d9-127">Идентификатор записи — это идентификатор операции 4-байтных MAPI для папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="e58d9-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="e58d9-128">Для получения дополнительных сведений см [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="e58d9-128">For more information, see [ENTRYID](http://msdn.microsoft.com/en-us/library/ms836424).</span></span>
  
<span data-ttu-id="e58d9-129">Когда поставщик хранения PST присваивает идентификатор записи в новый объект, сначала ему идентификатор GUID, идентифицирующий сервер и индекса, который определяет объект в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e58d9-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="e58d9-130">Несмотря на то, что идентификатор GUID не является уникальным для всех идентификаторы, GUID и индекса в сочетании предоставить уникальные запись.</span><span class="sxs-lookup"><span data-stu-id="e58d9-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="e58d9-131">Эта пара GUID и индекса отслеживается долгосрочного структуры кода **LTID**которого является частью структуры **OLFI** .</span><span class="sxs-lookup"><span data-stu-id="e58d9-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="e58d9-132">Поставщик хранения PST-файлов не сохраняются физически в **OLFI** структуру **LTID** для каждой пары GUID индекса.</span><span class="sxs-lookup"><span data-stu-id="e58d9-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="e58d9-133">Отслеживает структуры один **LTID** , *ltidAlloc* , в настоящее время первого доступные пары GUID индекса; count, *dwAlloc* , из числа доступных записей, общий доступ к этой же GUID; и второй структуры **LTID** , *ltidNextAlloc* , для следующего доступные пары GUID индекса, свой идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="e58d9-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="e58d9-134">PST хранения поставщиком структуры **OLFI** для отслеживания идентификаторов GUID и индексы, раздать. Виртуальный уровне поставщик поддерживает резерв числа структур **LTID** , готовые выделить.</span><span class="sxs-lookup"><span data-stu-id="e58d9-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="e58d9-135">*dwAlloc* содержит счетчик доступных структур **LTID** .</span><span class="sxs-lookup"><span data-stu-id="e58d9-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="e58d9-136">Запросы на идентификаторы поступают в блоках.</span><span class="sxs-lookup"><span data-stu-id="e58d9-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="e58d9-137">Если запрос для блока, поставщика хранилища PST-файлов проверяет наличие достаточных резерв в наличии путем сравнения запрошенный размер с *dwAlloc* .</span><span class="sxs-lookup"><span data-stu-id="e58d9-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="e58d9-138">Если имеется достаточно резерв, возвращает идентификатор GUID и индекса в *ltidAlloc* для выделения.</span><span class="sxs-lookup"><span data-stu-id="e58d9-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="e58d9-139">Уменьшение *dwAlloc* на запрошенный размер и увеличивает запрошенный размер индекса в *ltidAlloc* .</span><span class="sxs-lookup"><span data-stu-id="e58d9-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="e58d9-140">Это подготовит поставщика хранилища PST-файлов для выделения *ltidAlloc* при следующем запросе для другого блока идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="e58d9-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="e58d9-141">Обратите внимание на то, что идентификатор GUID остаются неизменными для следующего запроса.</span><span class="sxs-lookup"><span data-stu-id="e58d9-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="e58d9-142">Если размер запроса превышает *dwAlloc* , поставщик хранения PST пытается использовать, что она имеет далее в запасе в соответствии с *dwNextAlloc* и *ltidNextAlloc* .</span><span class="sxs-lookup"><span data-stu-id="e58d9-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="e58d9-143">Копирует *dwNextAlloc* и *ltidNextAlloc* *dwAlloc* и *ltidAlloc* соответственно и задает *dwNextAlloc* и *ltidNextAlloc* значение NULL.</span><span class="sxs-lookup"><span data-stu-id="e58d9-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="e58d9-144">Поставщик, который является оболочкой поставщика хранилища PST периодически должен проверить, *ltidNextAlloc* ли значения NULL.</span><span class="sxs-lookup"><span data-stu-id="e58d9-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="e58d9-145">Если он установлен, поставщик должен внесите в нее новый GUID и Сброс *dwNextAlloc* таким образом, могут быть выделены дополнительные записи идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="e58d9-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e58d9-146">См. также</span><span class="sxs-lookup"><span data-stu-id="e58d9-146">See also</span></span>



[<span data-ttu-id="e58d9-147">О репликации API</span><span class="sxs-lookup"><span data-stu-id="e58d9-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e58d9-148">О репликации конечного автомата</span><span class="sxs-lookup"><span data-stu-id="e58d9-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e58d9-149">LTID</span><span class="sxs-lookup"><span data-stu-id="e58d9-149">LTID</span></span>](ltid.md)

