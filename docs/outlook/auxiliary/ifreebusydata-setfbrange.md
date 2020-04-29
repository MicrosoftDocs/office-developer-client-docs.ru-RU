---
title: ифрибусидатасетфбранже
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Задает диапазон времени для перечисления свободных и занятых блоков данных для пользователя.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421664"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="1f180-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="1f180-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="1f180-104">Задает диапазон времени для перечисления свободных и занятых блоков данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f180-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1f180-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1f180-105">Quick info</span></span>

<span data-ttu-id="1f180-106">Обратитесь к разделу [ифрибусидата](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="1f180-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="1f180-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f180-107">Parameters</span></span>

<span data-ttu-id="1f180-108">_ртмстарт_</span><span class="sxs-lookup"><span data-stu-id="1f180-108">_rtmStart_</span></span>
  
> <span data-ttu-id="1f180-109">возврата Относительное значение времени начала сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="1f180-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="1f180-110">Это значение равно количеству минут, прошедших с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="1f180-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="1f180-111">_ртменд_</span><span class="sxs-lookup"><span data-stu-id="1f180-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="1f180-112">возврата Относительное значение времени завершения сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="1f180-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="1f180-113">Это значение равно количеству минут, прошедших с 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="1f180-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1f180-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1f180-114">Return values</span></span>

<span data-ttu-id="1f180-115">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="1f180-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f180-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f180-116">Remarks</span></span>

<span data-ttu-id="1f180-117">Этот метод используется для указания диапазона времени элементов календаря, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1f180-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="1f180-118">Значения *фтмстарт* и *фтменд* кэшируются и возвращаются при последующих вызовах [ифрибусидата:: жетфбпублишранже](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="1f180-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f180-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1f180-119">See also</span></span>

- [<span data-ttu-id="1f180-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="1f180-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="1f180-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="1f180-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="1f180-122">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="1f180-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

