---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возвращает для каждого указанного пользователя интерфейс для записи бесплатных и загруженных блоков данных в диапазоне времени.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411234"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="fde1a-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="fde1a-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="fde1a-104">Возвращает для каждого указанного пользователя интерфейс для записи бесплатных и загруженных блоков данных в диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="fde1a-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fde1a-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fde1a-105">Quick info</span></span>

<span data-ttu-id="fde1a-106">См. [в программе IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="fde1a-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="fde1a-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="fde1a-107">Parameters</span></span>

<span data-ttu-id="fde1a-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="fde1a-108">_cMax_</span></span>
  
> <span data-ttu-id="fde1a-109">[in] Количество возвращаемого [интерфейса IFreeBusyData.](ifreebusydata.md)</span><span class="sxs-lookup"><span data-stu-id="fde1a-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="fde1a-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="fde1a-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="fde1a-111">[in] Массив бесплатных и занятых пользователей для получения данных.</span><span class="sxs-lookup"><span data-stu-id="fde1a-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="fde1a-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="fde1a-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="fde1a-113">[in] [вышел] Массив интерфейсов **IFreeBusyData,** соответствующих массиву _rgfbuser_ структур [FBUser.](fbuser.md)</span><span class="sxs-lookup"><span data-stu-id="fde1a-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="fde1a-114">Этот массив указателей выделяется вызываемой и освобожден вызываемой.</span><span class="sxs-lookup"><span data-stu-id="fde1a-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="fde1a-115">Фактические интерфейсы, на которые указывается, выпускаются, когда вызываемая с ними работа.</span><span class="sxs-lookup"><span data-stu-id="fde1a-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="fde1a-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="fde1a-116">_phrStatus_</span></span>
  
> <span data-ttu-id="fde1a-117">[вышел] Массив результатов **HRESULT** для поиска каждого соответствующего **интерфейса IFreeBusyData.**</span><span class="sxs-lookup"><span data-stu-id="fde1a-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="fde1a-118">Значение может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="fde1a-118">The value may be NULL.</span></span> <span data-ttu-id="fde1a-119">Результат задан для S_OK, если  _соответствующая prgfbdata_ действительна.</span><span class="sxs-lookup"><span data-stu-id="fde1a-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="fde1a-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="fde1a-120">_pcRead_</span></span>
  
>  <span data-ttu-id="fde1a-121">[вышел] Фактическое число пользователей, для которых найден **интерфейс IFreeBusyData.**</span><span class="sxs-lookup"><span data-stu-id="fde1a-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fde1a-122">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fde1a-122">Return values</span></span>

<span data-ttu-id="fde1a-123">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="fde1a-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fde1a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fde1a-124">See also</span></span>

- [<span data-ttu-id="fde1a-125">Константы (API free/busy)</span><span class="sxs-lookup"><span data-stu-id="fde1a-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

