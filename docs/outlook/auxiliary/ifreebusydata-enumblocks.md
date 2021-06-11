---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Получает интерфейс, который указывает свободные и загруженные блоки данных для пользователя в указанном диапазоне времени.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317558"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="f779b-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="f779b-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="f779b-104">Получает интерфейс, который указывает свободные и загруженные блоки данных для пользователя в указанном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="f779b-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f779b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f779b-105">Quick info</span></span>

<span data-ttu-id="f779b-106">См. [iFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="f779b-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="f779b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f779b-107">Parameters</span></span>

<span data-ttu-id="f779b-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="f779b-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="f779b-109">[вышел] Интерфейс для переумерия бесплатных и занятых блоков.</span><span class="sxs-lookup"><span data-stu-id="f779b-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="f779b-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="f779b-110">_ftmStart_</span></span>
  
> <span data-ttu-id="f779b-111">[in] Время начала для переумерия.</span><span class="sxs-lookup"><span data-stu-id="f779b-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="f779b-112">Выражается в [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="f779b-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="f779b-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="f779b-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="f779b-114">[in] Время окончания для переумерия.</span><span class="sxs-lookup"><span data-stu-id="f779b-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="f779b-115">Выражается в **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="f779b-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f779b-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f779b-116">Return values</span></span>

<span data-ttu-id="f779b-117">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="f779b-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f779b-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f779b-118">Remarks</span></span>

<span data-ttu-id="f779b-119">Этот метод используется для указать диапазон времени элементов календаря, для которых можно получить сведения.</span><span class="sxs-lookup"><span data-stu-id="f779b-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="f779b-120">Значения  *ftmStart* и *ftmEnd* кэшировать и возвращать в последующем вызове [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="f779b-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="f779b-121">Бесплатный/занятый поставщик также может впоследствии использовать возвращенный [интерфейс IEnumFBBlock](ienumfbblock.md) для доступа к переумериям.</span><span class="sxs-lookup"><span data-stu-id="f779b-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f779b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f779b-122">See also</span></span>

- [<span data-ttu-id="f779b-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="f779b-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="f779b-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="f779b-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="f779b-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="f779b-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="f779b-126">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="f779b-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

