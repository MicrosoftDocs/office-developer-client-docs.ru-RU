---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345780"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="3ba8c-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="3ba8c-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="3ba8c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ba8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ba8c-105">Получает адрес функции выделения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ba8c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3ba8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="3ba8c-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="3ba8c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3ba8c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3ba8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3ba8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3ba8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3ba8c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3ba8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="3ba8c-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3ba8c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="3ba8c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ba8c-112">Parameters</span></span>

<span data-ttu-id="3ba8c-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="3ba8c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ba8c-114">Return value</span></span>

<span data-ttu-id="3ba8c-115">Функция **мапижетдефаултмаллок** возвращает указатель на функцию выделения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ba8c-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

