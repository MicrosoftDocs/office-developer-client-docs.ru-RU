---
title: Метод OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807315"
---
# <a name="opensession"></a><span data-ttu-id="9b607-103">Метод OpenSession</span><span class="sxs-lookup"><span data-stu-id="9b607-103">OpenSession</span></span>

<span data-ttu-id="9b607-104">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9b607-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9b607-105">Создает сеанс, в котором могут быть выполнены определенные пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="9b607-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="9b607-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9b607-106">Parameters</span></span>

<span data-ttu-id="9b607-107">_Параметры_</span><span class="sxs-lookup"><span data-stu-id="9b607-107">_Params_</span></span>
  
> <span data-ttu-id="9b607-108">Указатель, разделенных точкой с запятой строку ЮНИКОДА параметров для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="9b607-108">A pointer to semicolon-delimited UNICODE string of parameters for the session.</span></span> <span data-ttu-id="9b607-109">Excel не использует этот аргумент.</span><span class="sxs-lookup"><span data-stu-id="9b607-109">Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b607-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9b607-110">Return value</span></span>

<span data-ttu-id="9b607-111">Идентификатор сеанса для использования в других вызовов соединитель кластера, если сеанс был успешно создан; в противном случае — **xlHpcRetCallFailed**.</span><span class="sxs-lookup"><span data-stu-id="9b607-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b607-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9b607-112">See also</span></span>

- [<span data-ttu-id="9b607-113">Функции соединителя кластера Excel</span><span class="sxs-lookup"><span data-stu-id="9b607-113">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

