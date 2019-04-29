---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421839"
---
# <a name="opensession"></a><span data-ttu-id="6908a-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="6908a-103">OpenSession</span></span>

<span data-ttu-id="6908a-104">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6908a-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6908a-105">Создает сеанс, в котором можно выполнить пользовательские функции.</span><span class="sxs-lookup"><span data-stu-id="6908a-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="6908a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6908a-106">Parameters</span></span>

<span data-ttu-id="6908a-107">_Параметры_</span><span class="sxs-lookup"><span data-stu-id="6908a-107">_Params_</span></span>
  
> <span data-ttu-id="6908a-108">Указатель на строку параметров в Юникоде, разделенных точкой с запятой для сеанса.</span><span class="sxs-lookup"><span data-stu-id="6908a-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="6908a-109">В Excel этот аргумент не используется.</span><span class="sxs-lookup"><span data-stu-id="6908a-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6908a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6908a-110">Return value</span></span>

<span data-ttu-id="6908a-111">Идентификатор сеанса, используемый в других вызовах соединителя кластера, если сеанс был успешно создан; в противном случае **кслхпкреткаллфаилед**.</span><span class="sxs-lookup"><span data-stu-id="6908a-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6908a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6908a-112">See also</span></span>

- [<span data-ttu-id="6908a-113">Функции для работы с соединителями кластеров Excel</span><span class="sxs-lookup"><span data-stu-id="6908a-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

