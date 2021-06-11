---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062027"
---
# <a name="imapiinitmonitorisinitialized"></a><span data-ttu-id="71660-103">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="71660-103">IMAPIInitMonitor::IsInitialized</span></span>
  
<span data-ttu-id="71660-104">**Применяется к**: Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="71660-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="71660-105">Запрашивает MAPI, чтобы определить, инициализирована ли она в процессе вызова.</span><span class="sxs-lookup"><span data-stu-id="71660-105">Queries MAPI to determine if it currently initialized in the calling process.</span></span>

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a><span data-ttu-id="71660-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71660-106">Parameters</span></span>
<span data-ttu-id="71660-107">Нет</span><span class="sxs-lookup"><span data-stu-id="71660-107">None</span></span>

## <a name="return-value"></a><span data-ttu-id="71660-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71660-108">Return value</span></span>
<span data-ttu-id="71660-109">BoOL, указывающее текущее состояние инициализации MAPI, значение TRUE означает, что MAPI инициализирован и доступен для использования, в то время как значение FALSE означает, что MAPI является текущим и не готово к потреблению.</span><span class="sxs-lookup"><span data-stu-id="71660-109">A BOOL indicating the current state of MAPI initialization, a value of TRUE means MAPI has been initialized and is available for use, while a value of FALSE means MAPI is currenty uninitialized and is not ready be consumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="71660-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="71660-110">Remarks</span></span>
<span data-ttu-id="71660-111">Это можно использовать для определения готовности MAPI к применению, например, если приложение хотело что-то сделать, только если MAPI уже инициализирован, это может быть полезной проверкой фоновой задачи, чтобы предотвратить затраты на закрепление MAPI для необязательных работ.</span><span class="sxs-lookup"><span data-stu-id="71660-111">This can be used to determine if MAPI is ready to be used, for example, if your application wanted to do something only if MAPI has already be initialized, this could be a useful check in a background task to prevent the cost of spinning up MAPI for optional work.</span></span>

## <a name="see-also"></a><span data-ttu-id="71660-112">См. также</span><span class="sxs-lookup"><span data-stu-id="71660-112">See also</span></span>

[<span data-ttu-id="71660-113">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="71660-113">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="71660-114">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="71660-114">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
