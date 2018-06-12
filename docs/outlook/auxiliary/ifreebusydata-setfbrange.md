---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Задает диапазон времени для перечисления блоков данных о доступности для пользователя.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807732"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="7e56e-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="7e56e-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="7e56e-104">Задает диапазон времени для перечисления блоков данных о доступности для пользователя.</span><span class="sxs-lookup"><span data-stu-id="7e56e-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7e56e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7e56e-105">Quick info</span></span>

<span data-ttu-id="7e56e-106">В разделе [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="7e56e-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="7e56e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="7e56e-107">Parameters</span></span>

<span data-ttu-id="7e56e-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="7e56e-108">_rtmStart_</span></span>
  
> <span data-ttu-id="7e56e-109">[in] Значение относительно времени для начала сведения о доступности.</span><span class="sxs-lookup"><span data-stu-id="7e56e-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="7e56e-110">Это значение — число минут, начиная с 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="7e56e-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="7e56e-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="7e56e-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="7e56e-112">[in] Значение относительно времени в конце сведений о доступности.</span><span class="sxs-lookup"><span data-stu-id="7e56e-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="7e56e-113">Это значение — число минут, начиная с 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="7e56e-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7e56e-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7e56e-114">Return values</span></span>

<span data-ttu-id="7e56e-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="7e56e-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e56e-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="7e56e-116">Remarks</span></span>

<span data-ttu-id="7e56e-117">Этот метод используется для указания диапазона времени для элементов календаря, для которого нужно извлечь подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="7e56e-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="7e56e-118">Значения *ftmStart* и *ftmEnd* кэширования и возвращаются в последующих вызовов из [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="7e56e-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e56e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7e56e-119">See also</span></span>

- [<span data-ttu-id="7e56e-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="7e56e-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="7e56e-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="7e56e-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="7e56e-122">Использование относительных времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="7e56e-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

