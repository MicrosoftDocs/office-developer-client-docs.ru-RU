---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422539"
---
# <a name="closesession"></a><span data-ttu-id="92393-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="92393-103">CloseSession</span></span>

<span data-ttu-id="92393-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92393-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="92393-105">Завершает сеанс кластером.</span><span class="sxs-lookup"><span data-stu-id="92393-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="92393-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92393-106">Parameters</span></span>

<span data-ttu-id="92393-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="92393-107">_SessionId_</span></span>
  
> <span data-ttu-id="92393-108">ИД сеанса, который необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="92393-108">The ID of the session to close.</span></span> <span data-ttu-id="92393-109">Это значение должно соответствовать значению, возвращаемом [OpenSession.](opensession.md)</span><span class="sxs-lookup"><span data-stu-id="92393-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92393-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92393-110">Return value</span></span>

<span data-ttu-id="92393-111">**xlHpcRetSuccess,** если сеанс закрыт; **xlHpcRetInvalidSessionId,** если аргумент  _SessionId_ является недопустимым; **xlHpcRetCallFailed при** других сбоях.</span><span class="sxs-lookup"><span data-stu-id="92393-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92393-112">См. также</span><span class="sxs-lookup"><span data-stu-id="92393-112">See also</span></span>

- [<span data-ttu-id="92393-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="92393-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="92393-114">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="92393-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

