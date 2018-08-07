---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Получает интерфейс, который перечисляет занятости блоков данных для пользователя в рамках в заданном диапазоне времени.
ms.openlocfilehash: ab377b1029296b6b4bac68d7169dcf7b8dcd8b87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807719"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="8a128-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="8a128-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="8a128-104">Получает интерфейс, который перечисляет занятости блоков данных для пользователя в рамках в заданном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="8a128-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8a128-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8a128-105">Quick info</span></span>

<span data-ttu-id="8a128-106">В разделе [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="8a128-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="8a128-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a128-107">Parameters</span></span>

<span data-ttu-id="8a128-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="8a128-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="8a128-109">[out] Интерфейс для перечисления блоки сведениям о доступности.</span><span class="sxs-lookup"><span data-stu-id="8a128-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="8a128-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="8a128-110">_ftmStart_</span></span>
  
> <span data-ttu-id="8a128-111">[in] Время начала для перечисления.</span><span class="sxs-lookup"><span data-stu-id="8a128-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="8a128-112">Выражается в [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a128-112">It is expressed in [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="8a128-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="8a128-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="8a128-114">[in] Время окончания для перечисления.</span><span class="sxs-lookup"><span data-stu-id="8a128-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="8a128-115">Выражается в **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="8a128-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8a128-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8a128-116">Return values</span></span>

<span data-ttu-id="8a128-117">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="8a128-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a128-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="8a128-118">Remarks</span></span>

<span data-ttu-id="8a128-119">Этот метод используется для указания диапазона времени для элементов календаря, для которого нужно извлечь подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="8a128-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="8a128-120">Значения *ftmStart* и *ftmEnd* кэширования и возвращаются в последующих вызовов из [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="8a128-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="8a128-121">Обмен сведениями о доступности поставщика можно также последовательно использовать возвращенный интерфейс [IEnumFBBlock](ienumfbblock.md) для доступа к перечисления.</span><span class="sxs-lookup"><span data-stu-id="8a128-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a128-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8a128-122">See also</span></span>

- [<span data-ttu-id="8a128-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="8a128-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="8a128-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="8a128-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="8a128-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="8a128-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="8a128-126">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="8a128-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

