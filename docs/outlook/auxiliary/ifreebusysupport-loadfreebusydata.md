---
title: ифрибусисуппортлоадфрибусидата
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Возвращает для каждого указанного пользователя интерфейс для перечисления блоков сведений о занятости в пределах диапазона времени.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411234"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="f2c0e-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="f2c0e-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="f2c0e-104">Возвращает для каждого указанного пользователя интерфейс для перечисления блоков сведений о занятости в пределах диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f2c0e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f2c0e-105">Quick info</span></span>

<span data-ttu-id="f2c0e-106">Обратитесь к разделу [ифрибусисуппорт](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="f2c0e-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="f2c0e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2c0e-107">Parameters</span></span>

<span data-ttu-id="f2c0e-108">_кмакс_</span><span class="sxs-lookup"><span data-stu-id="f2c0e-108">_cMax_</span></span>
  
> <span data-ttu-id="f2c0e-109">возврата Число возвращаемых интерфейсов [ифрибусидата](ifreebusydata.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c0e-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="f2c0e-110">_ргфбусер_</span><span class="sxs-lookup"><span data-stu-id="f2c0e-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="f2c0e-111">возврата Массив пользователей сведений о занятости для получения данных.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="f2c0e-112">_пргфбдата_</span><span class="sxs-lookup"><span data-stu-id="f2c0e-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="f2c0e-113">возврата вышли Массив интерфейсов **ифрибусидата** , соответствующих массиву _ргфбусер_ структуры [фбусер](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c0e-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f2c0e-114">Этот массив указателей выделяется вызывающим и освобождается вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="f2c0e-115">Фактические интерфейсы, на которые указывает, освобождаются, когда вызывающая сторона выполнила их.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="f2c0e-116">_фрстатус_</span><span class="sxs-lookup"><span data-stu-id="f2c0e-116">_phrStatus_</span></span>
  
> <span data-ttu-id="f2c0e-117">вышли Массив результатов **HRESULT** для получения каждого соответствующего интерфейса **ифрибусидата** .</span><span class="sxs-lookup"><span data-stu-id="f2c0e-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="f2c0e-118">Значение может быть равно NULL.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-118">The value may be NULL.</span></span> <span data-ttu-id="f2c0e-119">Результат имеет значение S_OK, если соответствующий _пргфбдата_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="f2c0e-120">_пкреад_</span><span class="sxs-lookup"><span data-stu-id="f2c0e-120">_pcRead_</span></span>
  
>  <span data-ttu-id="f2c0e-121">вышли Фактическое количество пользователей, для которых был найден интерфейс **ифрибусидата** .</span><span class="sxs-lookup"><span data-stu-id="f2c0e-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f2c0e-122">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f2c0e-122">Return values</span></span>

<span data-ttu-id="f2c0e-123">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="f2c0e-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2c0e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f2c0e-124">See also</span></span>

- [<span data-ttu-id="f2c0e-125">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="f2c0e-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

