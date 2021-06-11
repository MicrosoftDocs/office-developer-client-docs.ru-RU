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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438206"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="ee7e0-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="ee7e0-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="ee7e0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee7e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee7e0-105">Извлекает адрес функции распределения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee7e0-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee7e0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ee7e0-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee7e0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ee7e0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ee7e0-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ee7e0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee7e0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee7e0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee7e0-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ee7e0-110">Called by:</span></span>  <br/> |<span data-ttu-id="ee7e0-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ee7e0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="ee7e0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee7e0-112">Parameters</span></span>

<span data-ttu-id="ee7e0-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="ee7e0-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="ee7e0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee7e0-114">Return value</span></span>

<span data-ttu-id="ee7e0-115">Функция **MAPIGetDefaultMalloc** возвращает указатель к функции распределения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee7e0-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

