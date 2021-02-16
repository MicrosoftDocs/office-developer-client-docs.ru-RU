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
# <a name="olfi"></a><span data-ttu-id="31ff5-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="31ff5-103">OLFI</span></span>

  
  
<span data-ttu-id="31ff5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31ff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31ff5-105">Очередь структур долгосрочных ИД, используемых поставщиком файлов личных папок (PST) для назначения ИД записи для нового сообщения или папки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="31ff5-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="31ff5-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="31ff5-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="31ff5-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="31ff5-107">Members</span></span>

 <span data-ttu-id="31ff5-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="31ff5-108">_ulVersion_</span></span>
  
- <span data-ttu-id="31ff5-109">Номер версии структуры.</span><span class="sxs-lookup"><span data-stu-id="31ff5-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="31ff5-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="31ff5-110">_muidReserved_</span></span>
  
- <span data-ttu-id="31ff5-111">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="31ff5-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="31ff5-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="31ff5-112">_ulReserved_</span></span>
  
- <span data-ttu-id="31ff5-113">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="31ff5-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="31ff5-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="31ff5-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="31ff5-115">Количество записей, доступных для выделения.</span><span class="sxs-lookup"><span data-stu-id="31ff5-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="31ff5-116">Эти записи имеют один и тот же глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="31ff5-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="31ff5-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="31ff5-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="31ff5-118">Количество записей, доступных далее для выделения.</span><span class="sxs-lookup"><span data-stu-id="31ff5-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="31ff5-119">Эти записи имеют один и тот же GUID.</span><span class="sxs-lookup"><span data-stu-id="31ff5-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="31ff5-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="31ff5-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="31ff5-121">Структура долгосрочных ИД, **[LTID,](ltid.md)** определяющие запись, доступную в настоящее время для выделения.</span><span class="sxs-lookup"><span data-stu-id="31ff5-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="31ff5-122">Структура долгосрочного ИД содержит GUID и индекс, идентифицирующий объект в хранилище.</span><span class="sxs-lookup"><span data-stu-id="31ff5-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="31ff5-123">Вместе GUID и индекс могут сформировать уникальный ИД записи для объекта.</span><span class="sxs-lookup"><span data-stu-id="31ff5-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="31ff5-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="31ff5-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="31ff5-125">Структура долгосрочных ИД, определяющие следующую доступную запись.</span><span class="sxs-lookup"><span data-stu-id="31ff5-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31ff5-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="31ff5-126">Remarks</span></span>

<span data-ttu-id="31ff5-127">Идентификатор записи — это четырехбайтовый идентификатор записи MAPI для папки или сообщения.</span><span class="sxs-lookup"><span data-stu-id="31ff5-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="31ff5-128">Дополнительные сведения см. в [entryID.](https://msdn.microsoft.com/library/ms836424)</span><span class="sxs-lookup"><span data-stu-id="31ff5-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="31ff5-129">Когда поставщик PST-хранения назначает идентификатор записи новому объекту, ему сначала требуется ИДЕНТИФИКАТОР GUID, определяя сервер, и индекс, идентифицируя объект в хранилище.</span><span class="sxs-lookup"><span data-stu-id="31ff5-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="31ff5-130">Хотя GUID не является уникальным для всех ИД записей, guID и индекс в сочетании предоставляют уникальную запись.</span><span class="sxs-lookup"><span data-stu-id="31ff5-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="31ff5-131">Эта пара GUID и индекса отслеживается по долгосрочной структуре **ID, LTID,** которая является частью **структуры OLFI.**</span><span class="sxs-lookup"><span data-stu-id="31ff5-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="31ff5-132">Поставщик PST-хранения физически не сохраняет в **OLFI** **структуру LTID** для каждой пары GUID-index.</span><span class="sxs-lookup"><span data-stu-id="31ff5-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="31ff5-133">Он сохраняет одну **структуру LTID,**  *ltidAlloc,*  для первой доступной в настоящее время пары GUID-index; число ,  *dwAlloc*  , количество доступных записей, которые имеют один и тот же GUID; и вторая **структура LTID,**  *ltidNextAlloc,*  для следующей доступной пары GUID-index с другим GUID.</span><span class="sxs-lookup"><span data-stu-id="31ff5-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="31ff5-134">Поставщик PST-хранения использует структуру **OLFI** для отслеживания переданных им GUID и индексов. На виртуальном уровне поставщик сохраняет резерв нескольких структур **LTID,** готовых к выделению.</span><span class="sxs-lookup"><span data-stu-id="31ff5-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="31ff5-135">*dwAlloc* поддерживает количество доступных структур **LTID.**</span><span class="sxs-lookup"><span data-stu-id="31ff5-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="31ff5-136">Запросы на ввод ИД приходят в блоках.</span><span class="sxs-lookup"><span data-stu-id="31ff5-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="31ff5-137">При запросе блокировки поставщик PST-магазина проверяет наличие достаточного резерва, сравнивая запрашиваемые размеры с *dwAlloc.*</span><span class="sxs-lookup"><span data-stu-id="31ff5-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="31ff5-138">Если резерва достаточно, он возвращает GUID и индекс  *в ltidAlloc для*  выделения.</span><span class="sxs-lookup"><span data-stu-id="31ff5-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="31ff5-139">Затем он уменьшает  *dwAlloc*  на запрашиваемую величину и приращение индекса  *в ltidAlloc*  на запрашиваемую величину.</span><span class="sxs-lookup"><span data-stu-id="31ff5-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="31ff5-140">Это подготавливает поставщика ltidAlloc к выделению  *ltidAlloc*  в следующем запросе для другого блока ID записей.</span><span class="sxs-lookup"><span data-stu-id="31ff5-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="31ff5-141">Обратите внимание, что GUID для следующего запроса остается таким же.</span><span class="sxs-lookup"><span data-stu-id="31ff5-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="31ff5-142">Если размер запроса превышает  *dwAlloc,*  поставщик PST-магазина пытается использовать то, что у него есть в резерве, как указано  *в dwNextAlloc*  и  *ltidNextAlloc*  .</span><span class="sxs-lookup"><span data-stu-id="31ff5-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="31ff5-143">Он копирует  *dwNextAlloc*  и  *ltidNextAlloc*  в  *dwAlloc*  и  *ltidAlloc*  соответственно, а также устанавливает  *для dwNextAlloc*  и  *ltidNextAlloc*  nULL.</span><span class="sxs-lookup"><span data-stu-id="31ff5-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="31ff5-144">Поставщик, который обтекает поставщика PST-магазина, должен периодически проверять  *ltidNextAlloc,*  чтобы узнать, имеет ли он NULL.</span><span class="sxs-lookup"><span data-stu-id="31ff5-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="31ff5-145">В этом случае поставщик должен заполнить его новым GUID и сбросить  *dwNextAlloc,*  чтобы можно было выделить дополнительные ИД записей.</span><span class="sxs-lookup"><span data-stu-id="31ff5-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31ff5-146">См. также</span><span class="sxs-lookup"><span data-stu-id="31ff5-146">See also</span></span>



[<span data-ttu-id="31ff5-147">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="31ff5-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="31ff5-148">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="31ff5-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="31ff5-149">LTID</span><span class="sxs-lookup"><span data-stu-id="31ff5-149">LTID</span></span>](ltid.md)

