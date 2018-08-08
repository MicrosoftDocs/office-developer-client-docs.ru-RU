---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Получает указанного интервала времени для перечисления сведений о доступности блоков данных для пользователя.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807714"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="93542-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="93542-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="93542-104">Получает указанного интервала времени для перечисления сведений о доступности блоков данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="93542-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="93542-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="93542-105">Quick info</span></span>

<span data-ttu-id="93542-106">В разделе [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="93542-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="93542-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="93542-107">Parameters</span></span>

<span data-ttu-id="93542-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="93542-108">_prtmStart_</span></span>
  
> <span data-ttu-id="93542-109">[out] Значение относительно времени для начала сведения о доступности.</span><span class="sxs-lookup"><span data-stu-id="93542-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="93542-110">Это значение — число минут, начиная с 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="93542-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="93542-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="93542-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="93542-112">[out] Значение относительно времени в конце сведений о доступности.</span><span class="sxs-lookup"><span data-stu-id="93542-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="93542-113">Это значение — число минут, начиная с 1 января 1601.</span><span class="sxs-lookup"><span data-stu-id="93542-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="93542-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="93542-114">Return values</span></span>

<span data-ttu-id="93542-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="93542-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93542-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="93542-116">Remarks</span></span>

<span data-ttu-id="93542-117">Обмен сведениями о доступности поставщик вызывает [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , чтобы задать интервал для перечисления.</span><span class="sxs-lookup"><span data-stu-id="93542-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="93542-118">Если не был вызван [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , значения по умолчанию для **prtmStart** и **prtmEnd** должно иметь значение между 1 апреля 1601 00:00:00Z и 31 августа 4500 11:59:59Z соответственно.</span><span class="sxs-lookup"><span data-stu-id="93542-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="93542-119">Кроме того не следует устанавливать время начала должно быть больше времени окончания.</span><span class="sxs-lookup"><span data-stu-id="93542-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="93542-120">**IFreeBusyData::GetFBPublishRange** должен возвращать набора кэшированных значений в диапазоне времени с самыми последними звонка для **IFreeBusyData::EnumBlocks** или **IFreeBusyData::SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="93542-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93542-121">См. также</span><span class="sxs-lookup"><span data-stu-id="93542-121">See also</span></span>

- [<span data-ttu-id="93542-122">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="93542-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="93542-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="93542-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="93542-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="93542-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

