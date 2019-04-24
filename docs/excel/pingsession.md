---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301619"
---
# <a name="pingsession"></a><span data-ttu-id="6ee29-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="6ee29-103">PingSession</span></span>

<span data-ttu-id="6ee29-104">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6ee29-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6ee29-105">Проверяет, является ли сеанс допустимым.</span><span class="sxs-lookup"><span data-stu-id="6ee29-105">Checks whether a session is valid.</span></span> <span data-ttu-id="6ee29-106">Эта функция обычно вызывается, когда Excel должен определить, является ли ранее возвращенный идентификатор сеанса активным и может использоваться.</span><span class="sxs-lookup"><span data-stu-id="6ee29-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="6ee29-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ee29-107">Parameters</span></span>

<span data-ttu-id="6ee29-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="6ee29-108">_SessionID_</span></span>
  
> <span data-ttu-id="6ee29-109">Идентификатор сеанса, для которого проверяется связь.</span><span class="sxs-lookup"><span data-stu-id="6ee29-109">The ID of the session to ping.</span></span> <span data-ttu-id="6ee29-110">Это значение должно быть равно ИДЕНТИФИКАТОРу, возвращенному при предыдущем вызове [опенсессион](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="6ee29-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ee29-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ee29-111">Return value</span></span>

<span data-ttu-id="6ee29-112">**кслхпкретсукцесс** , если аргумент _SessionID_ является допустимым; в противном случае **кслхпкретинвалидсессионид**.</span><span class="sxs-lookup"><span data-stu-id="6ee29-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ee29-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6ee29-113">See also</span></span>

- [<span data-ttu-id="6ee29-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="6ee29-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="6ee29-115">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="6ee29-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

