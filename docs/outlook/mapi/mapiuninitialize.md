---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567393"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="3cc8c-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="3cc8c-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="3cc8c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cc8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cc8c-105">Уменьшает счетчик ссылок, очищает и удаления каждого экземпляра глобальных данных для библиотеки DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="3cc8c-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3cc8c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3cc8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="3cc8c-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="3cc8c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3cc8c-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="3cc8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3cc8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3cc8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3cc8c-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="3cc8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="3cc8c-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="3cc8c-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="3cc8c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cc8c-112">Parameters</span></span>

<span data-ttu-id="3cc8c-113">None</span><span class="sxs-lookup"><span data-stu-id="3cc8c-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="3cc8c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cc8c-114">Return value</span></span>

<span data-ttu-id="3cc8c-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="3cc8c-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3cc8c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="3cc8c-116">Remarks</span></span>

<span data-ttu-id="3cc8c-117">Клиентское приложение вызывает функцию **MAPIUninitialize** окончания его взаимодействия с MAPI, начиная с вызова функции [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="3cc8c-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="3cc8c-118">После вызова **MAPIUninitialize** нет других вызовов MAPI невозможны клиентом.</span><span class="sxs-lookup"><span data-stu-id="3cc8c-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="3cc8c-119">**MAPIUninitialize** уменьшает счетчик ссылок и соответствующую функцию **MAPIInitialize** увеличивает счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="3cc8c-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="3cc8c-120">Таким образом количество вызовов на одной функции должно совпадать с количеством вызовов в другой.</span><span class="sxs-lookup"><span data-stu-id="3cc8c-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3cc8c-121">В функции Win32 **DllMain** или любых других функций, который создает или завершение работы потоков не может вызывать **MAPIInitialize** или **MAPIUninitialize** из.</span><span class="sxs-lookup"><span data-stu-id="3cc8c-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="3cc8c-122">Дополнительные сведения можно [С помощью объектов являющихся потокобезопасными](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3cc8c-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

