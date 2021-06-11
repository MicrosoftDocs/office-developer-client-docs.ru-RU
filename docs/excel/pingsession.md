---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408364"
---
# <a name="pingsession"></a><span data-ttu-id="886f8-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="886f8-103">PingSession</span></span>

<span data-ttu-id="886f8-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="886f8-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="886f8-105">Проверяет, является ли сеанс допустимым.</span><span class="sxs-lookup"><span data-stu-id="886f8-105">Checks whether a session is valid.</span></span> <span data-ttu-id="886f8-106">Эта функция обычно называется, Excel необходимо определить, активен ли ранее возвращенный ID сеанса и можно ли его использовать.</span><span class="sxs-lookup"><span data-stu-id="886f8-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="886f8-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="886f8-107">Parameters</span></span>

<span data-ttu-id="886f8-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="886f8-108">_SessionID_</span></span>
  
> <span data-ttu-id="886f8-109">ID сеанса для ping.</span><span class="sxs-lookup"><span data-stu-id="886f8-109">The ID of the session to ping.</span></span> <span data-ttu-id="886f8-110">Это значение должно совпадать с ИД, возвращенным предыдущим вызовом [в OpenSession.](opensession.md)</span><span class="sxs-lookup"><span data-stu-id="886f8-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="886f8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="886f8-111">Return value</span></span>

<span data-ttu-id="886f8-112">**xlHpcRetSuccess,** если аргумент  _SessionId_ действителен; в **противном случае xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="886f8-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="886f8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="886f8-113">See also</span></span>

- [<span data-ttu-id="886f8-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="886f8-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="886f8-115">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="886f8-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

