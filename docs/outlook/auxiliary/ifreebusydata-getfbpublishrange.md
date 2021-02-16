---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Получает заранее заранее задав диапазон времени для перенамерения блоков данных о занятости для пользователя.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430079"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="291df-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="291df-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="291df-104">Получает заранее заранее задав диапазон времени для перенамерения блоков данных о занятости для пользователя.</span><span class="sxs-lookup"><span data-stu-id="291df-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="291df-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="291df-105">Quick info</span></span>

<span data-ttu-id="291df-106">См. [IFreeBusyData.](ifreebusydata.md)</span><span class="sxs-lookup"><span data-stu-id="291df-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="291df-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="291df-107">Parameters</span></span>

<span data-ttu-id="291df-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="291df-108">_prtmStart_</span></span>
  
> <span data-ttu-id="291df-109">[out] Относительное значение времени начала сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="291df-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="291df-110">Это значение является числом минут с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="291df-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="291df-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="291df-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="291df-112">[out] Относительное значение времени для окончания сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="291df-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="291df-113">Это значение — количество минут с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="291df-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="291df-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="291df-114">Return values</span></span>

<span data-ttu-id="291df-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="291df-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="291df-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="291df-116">Remarks</span></span>

<span data-ttu-id="291df-117">Поставщик услуг занятости вызывает [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange,](ifreebusydata-setfbrange.md) чтобы установить диапазон времени для нумерации.</span><span class="sxs-lookup"><span data-stu-id="291df-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="291df-118">Если не был вызван [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) или [IFreeBusyData::SetFBRange,](ifreebusydata-setfbrange.md) значения по умолчанию для **prtmStart** и **prtmEnd** должны быть заданы между 1 апреля 1601 г. 00:00:00Z и 31 августа 4500 11:59:59Z соответственно.</span><span class="sxs-lookup"><span data-stu-id="291df-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="291df-119">Кроме того, не следует устанавливать время начала больше времени окончания.</span><span class="sxs-lookup"><span data-stu-id="291df-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="291df-120">**IFreeBusyData::GetFBPublishRange** должен возвращать кэшданные значения для диапазона времени, заданного последним вызовом **IFreeBusyData::EnumBlocks** или **IFreeBusyData::SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="291df-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="291df-121">См. также</span><span class="sxs-lookup"><span data-stu-id="291df-121">See also</span></span>

- [<span data-ttu-id="291df-122">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="291df-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="291df-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="291df-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="291df-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="291df-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

