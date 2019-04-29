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
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408525"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="e1d1f-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="e1d1f-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="e1d1f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1d1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1d1f-105">Уменьшает значение счетчика ссылок, очищает и удаляет глобальные данные для библиотеки MAPI DLL.</span><span class="sxs-lookup"><span data-stu-id="e1d1f-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1d1f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e1d1f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1d1f-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="e1d1f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e1d1f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e1d1f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1d1f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1d1f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1d1f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e1d1f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e1d1f-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e1d1f-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="e1d1f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1d1f-112">Parameters</span></span>

<span data-ttu-id="e1d1f-113">Нет</span><span class="sxs-lookup"><span data-stu-id="e1d1f-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="e1d1f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1d1f-114">Return value</span></span>

<span data-ttu-id="e1d1f-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="e1d1f-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1d1f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1d1f-116">Remarks</span></span>

<span data-ttu-id="e1d1f-117">Клиентское приложение вызывает функцию **мапиунинитиализе** , чтобы завершить взаимодействие с MAPI, а затем вызовом функции [мапиинитиализе](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d1f-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="e1d1f-118">После вызова **мапиунинитиализе** клиент не может выполнять другие вызовы MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1d1f-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="e1d1f-119">**Мапиунинитиализе** уменьшает значение счетчика ссылок, а соответствующая функция **мапиинитиализе** увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="e1d1f-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="e1d1f-120">Таким образом, число вызовов одной функции должно равняться числу вызовов другой.</span><span class="sxs-lookup"><span data-stu-id="e1d1f-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1d1f-121">Вы не можете вызывать **мапиинитиализе** или **Мапиунинитиализе** из функции Win32 **DllMain** или любой другой функции, создающей или завершающей потоки.</span><span class="sxs-lookup"><span data-stu-id="e1d1f-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="e1d1f-122">Более подробную информацию можно узнать [в статье Использование потокобезопасных объектов](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e1d1f-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

