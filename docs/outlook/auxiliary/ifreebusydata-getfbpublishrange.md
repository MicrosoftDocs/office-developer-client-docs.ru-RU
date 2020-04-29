---
title: ифрибусидатажетфбпублишранже
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Получает предварительно заданный диапазон времени для перечисления блоков сведений о занятости для пользователя.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430079"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="24dec-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="24dec-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="24dec-104">Получает предварительно заданный диапазон времени для перечисления блоков сведений о занятости для пользователя.</span><span class="sxs-lookup"><span data-stu-id="24dec-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="24dec-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="24dec-105">Quick info</span></span>

<span data-ttu-id="24dec-106">Обратитесь к разделу [ифрибусидата](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="24dec-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="24dec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24dec-107">Parameters</span></span>

<span data-ttu-id="24dec-108">_пртмстарт_</span><span class="sxs-lookup"><span data-stu-id="24dec-108">_prtmStart_</span></span>
  
> <span data-ttu-id="24dec-109">вышли Относительное значение времени начала сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="24dec-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="24dec-110">Это значение равно количеству минут, прошедших с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="24dec-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="24dec-111">_пртменд_</span><span class="sxs-lookup"><span data-stu-id="24dec-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="24dec-112">вышли Относительное значение времени завершения сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="24dec-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="24dec-113">Это значение равно количеству минут, прошедших с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="24dec-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="24dec-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="24dec-114">Return values</span></span>

<span data-ttu-id="24dec-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="24dec-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24dec-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="24dec-116">Remarks</span></span>

<span data-ttu-id="24dec-117">Поставщик сведений о доступности вызывает [ифрибусидата:: енумблоккс](ifreebusydata-enumblocks.md) или [Ифрибусидата:: сетфбранже](ifreebusydata-setfbrange.md) , чтобы задать диапазон времени для перечисления.</span><span class="sxs-lookup"><span data-stu-id="24dec-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="24dec-118">Если [ифрибусидата:: енумблоккс](ifreebusydata-enumblocks.md) или [Ифрибусидата:: сетфбранже](ifreebusydata-setfbrange.md) не вызывался, значения по умолчанию для **пртмстарт** и **Пртменд** должны быть заданы между 1 апреля 1601 00:00:00Z и 31 августа 4500 11:59:59Z соответственно.</span><span class="sxs-lookup"><span data-stu-id="24dec-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="24dec-119">Кроме того, не следует устанавливать время начала, превышающее время окончания.</span><span class="sxs-lookup"><span data-stu-id="24dec-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="24dec-120">**Ифрибусидата:: жетфбпублишранже** должны возвращать кэшированные значения для диапазона времени, установленного самым последним вызовом для **Ифрибусидата:: енумблоккс** или **ифрибусидата:: сетфбранже**.</span><span class="sxs-lookup"><span data-stu-id="24dec-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24dec-121">См. также</span><span class="sxs-lookup"><span data-stu-id="24dec-121">See also</span></span>

- [<span data-ttu-id="24dec-122">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="24dec-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="24dec-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="24dec-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="24dec-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="24dec-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

