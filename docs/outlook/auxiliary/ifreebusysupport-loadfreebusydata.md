---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возврат значения, для каждого указанного пользователя, интерфейс для перечисления сведений о доступности блоков данных в интервал времени.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807717"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="4806e-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="4806e-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="4806e-104">Возврат значения, для каждого указанного пользователя, интерфейс для перечисления сведений о доступности блоков данных в интервал времени.</span><span class="sxs-lookup"><span data-stu-id="4806e-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4806e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4806e-105">Quick info</span></span>

<span data-ttu-id="4806e-106">В разделе [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="4806e-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="4806e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4806e-107">Parameters</span></span>

<span data-ttu-id="4806e-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="4806e-108">_cMax_</span></span>
  
> <span data-ttu-id="4806e-109">[in] Число интерфейсов [IFreeBusyData](ifreebusydata.md) для возврата.</span><span class="sxs-lookup"><span data-stu-id="4806e-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="4806e-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="4806e-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="4806e-111">[in] Массив пользователей о доступности для извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="4806e-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="4806e-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="4806e-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="4806e-113">[in] [out] Массив **IFreeBusyData** интерфейсы, которые соответствуют _rgfbuser_ массив структур [FBUser](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="4806e-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="4806e-114">Этот массив указателей, выделенный вызывающим абонентом и вызывающая.</span><span class="sxs-lookup"><span data-stu-id="4806e-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="4806e-115">Фактические интерфейсов, на который указывает, снимаются, когда выполняется с их помощью вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="4806e-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="4806e-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="4806e-116">_phrStatus_</span></span>
  
> <span data-ttu-id="4806e-117">[out] Массив **HRESULT** результатов для получения каждой соответствующий интерфейс **IFreeBusyData** .</span><span class="sxs-lookup"><span data-stu-id="4806e-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="4806e-118">Значение может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="4806e-118">The value may be NULL.</span></span> <span data-ttu-id="4806e-119">Результат имеет значение S_OK, если соответствующий _prgfbdata_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="4806e-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="4806e-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="4806e-120">_pcRead_</span></span>
  
>  <span data-ttu-id="4806e-121">[out] Фактическое число пользователей, для которых был найден интерфейс **IFreeBusyData** .</span><span class="sxs-lookup"><span data-stu-id="4806e-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4806e-122">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4806e-122">Return values</span></span>

<span data-ttu-id="4806e-123">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="4806e-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4806e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="4806e-124">See also</span></span>

- [<span data-ttu-id="4806e-125">Константы (занятости API)</span><span class="sxs-lookup"><span data-stu-id="4806e-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

