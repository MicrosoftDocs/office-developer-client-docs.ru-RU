---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 31b2353b76bbac5cd58cd791f4a289c7dbabdb78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809863"
---
# <a name="mapiinit0"></a><span data-ttu-id="bafce-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="bafce-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="bafce-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bafce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bafce-105">Передает параметры в функцию [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="bafce-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bafce-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bafce-106">Header file:</span></span>  <br/> |<span data-ttu-id="bafce-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="bafce-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="bafce-108">Members</span><span class="sxs-lookup"><span data-stu-id="bafce-108">Members</span></span>

 <span data-ttu-id="bafce-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="bafce-109">**ulVersion**</span></span>
  
> <span data-ttu-id="bafce-110">Целочисленное значение, представляющее номер версии структуры **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="bafce-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="bafce-111">Член **ulVersion** будущее расширение и не представляет версию интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="bafce-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="bafce-112">На данный момент **ulVersion** должен иметь значение MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="bafce-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="bafce-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="bafce-113">**ulFlags**</span></span>
  
> <span data-ttu-id="bafce-114">Битовая маска флаги, используемые для управления инициализации сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="bafce-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="bafce-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="bafce-115">The following flags can be set:</span></span>
    
<span data-ttu-id="bafce-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="bafce-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="bafce-117">MAPI следует создавать с помощью потока, посвященного уведомлений обработки вместо первого потока, используемый для вызова **MAPIInitialize**уведомления.</span><span class="sxs-lookup"><span data-stu-id="bafce-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="bafce-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="bafce-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="bafce-119">Звонящий выполняется как служба Windows.</span><span class="sxs-lookup"><span data-stu-id="bafce-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="bafce-120">Вызывающие объекты, которые не выполняется как служба Windows не следует устанавливать этот флаг; вызывающие объекты, на которых выполняется как служба необходимо установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="bafce-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="bafce-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="bafce-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="bafce-122">Задайте флаг MAPI_NO_COINT, чтобы **MAPIInitialize** не пытается инициализировать COM с помощью вызова [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="bafce-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="bafce-123">Если структуры **MAPIINIT_0** передается в **MAPIInitialize** с _ulFlags_ , задайте значение MAPI_NO_COINIT, MAPI будет предполагать, что COM уже инициализирована и обходили вызова **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="bafce-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bafce-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="bafce-124">Remarks</span></span>

<span data-ttu-id="bafce-125">Многопоточные клиентов следует устанавливать флаг MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="bafce-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="bafce-126">Если флажок не установлен, в потоке, используемом для первого вызова к **MAPIInitialize**создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bafce-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="bafce-127">Дополнительные сведения о реализации потокобезопасность в клиенте и когда установить этот флаг можно [Threading в MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="bafce-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bafce-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bafce-128">See also</span></span>



[<span data-ttu-id="bafce-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="bafce-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="bafce-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bafce-130">MAPI Structures</span></span>](mapi-structures.md)

