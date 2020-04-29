---
title: ифрибусидатаенумблоккс
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Получает интерфейс, который перечисляет блоки данных о занятости для пользователя в указанном диапазоне времени.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317558"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="30f43-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="30f43-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="30f43-104">Получает интерфейс, который перечисляет блоки данных о занятости для пользователя в указанном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="30f43-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30f43-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="30f43-105">Quick info</span></span>

<span data-ttu-id="30f43-106">Обратитесь к разделу [ифрибусидата](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="30f43-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="30f43-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="30f43-107">Parameters</span></span>

<span data-ttu-id="30f43-108">_ппенумфб_</span><span class="sxs-lookup"><span data-stu-id="30f43-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="30f43-109">вышли Интерфейс для перечисления блоков занятости.</span><span class="sxs-lookup"><span data-stu-id="30f43-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="30f43-110">_фтмстарт_</span><span class="sxs-lookup"><span data-stu-id="30f43-110">_ftmStart_</span></span>
  
> <span data-ttu-id="30f43-111">возврата Время начала перечисления.</span><span class="sxs-lookup"><span data-stu-id="30f43-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="30f43-112">Он выражается в [fileTime](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="30f43-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="30f43-113">_фтменд_</span><span class="sxs-lookup"><span data-stu-id="30f43-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="30f43-114">возврата Время окончания перечисления.</span><span class="sxs-lookup"><span data-stu-id="30f43-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="30f43-115">Он выражается в **fileTime**.</span><span class="sxs-lookup"><span data-stu-id="30f43-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="30f43-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="30f43-116">Return values</span></span>

<span data-ttu-id="30f43-117">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="30f43-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30f43-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="30f43-118">Remarks</span></span>

<span data-ttu-id="30f43-119">Этот метод используется для указания диапазона времени элементов календаря, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="30f43-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="30f43-120">Значения *фтмстарт* и *фтменд* кэшируются и возвращаются при последующих вызовах [ифрибусидата:: жетфбпублишранже](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="30f43-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="30f43-121">Поставщик сведений о доступности также может впоследствии использовать возвращенный интерфейс [иенумфбблокк](ienumfbblock.md) для доступа к перечислению.</span><span class="sxs-lookup"><span data-stu-id="30f43-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30f43-122">См. также</span><span class="sxs-lookup"><span data-stu-id="30f43-122">See also</span></span>

- [<span data-ttu-id="30f43-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="30f43-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="30f43-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="30f43-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="30f43-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="30f43-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="30f43-126">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="30f43-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

