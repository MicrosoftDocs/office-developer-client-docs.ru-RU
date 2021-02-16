---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Задает диапазон времени для enumeration of free/busy blocks of data for a user.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421664"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="20df8-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="20df8-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="20df8-104">Задает диапазон времени для enumeration of free/busy blocks of data for a user.</span><span class="sxs-lookup"><span data-stu-id="20df8-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="20df8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="20df8-105">Quick info</span></span>

<span data-ttu-id="20df8-106">См. [IFreeBusyData.](ifreebusydata.md)</span><span class="sxs-lookup"><span data-stu-id="20df8-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="20df8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20df8-107">Parameters</span></span>

<span data-ttu-id="20df8-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="20df8-108">_rtmStart_</span></span>
  
> <span data-ttu-id="20df8-109">[in] Относительное значение времени начала сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="20df8-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="20df8-110">Это значение является числом минут с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="20df8-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="20df8-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="20df8-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="20df8-112">[in] Относительное значение времени для окончания сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="20df8-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="20df8-113">Это значение является числом минут с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="20df8-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="20df8-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="20df8-114">Return values</span></span>

<span data-ttu-id="20df8-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="20df8-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20df8-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="20df8-116">Remarks</span></span>

<span data-ttu-id="20df8-117">Этот метод используется для указать диапазон времени элементов календаря, для которых необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="20df8-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="20df8-118">Значения *ftmStart* и *ftmEnd* кэшются и возвращаются при последующем вызове [IFreeBusyData::GetFBPublishRange.](ifreebusydata-getfbpublishrange.md)</span><span class="sxs-lookup"><span data-stu-id="20df8-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20df8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="20df8-119">See also</span></span>

- [<span data-ttu-id="20df8-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="20df8-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="20df8-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="20df8-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="20df8-122">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="20df8-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

