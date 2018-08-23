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
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592334"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="7bad0-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="7bad0-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="7bad0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bad0-105">Получает адрес функции выделения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bad0-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bad0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7bad0-106">Header file:</span></span>  <br/> |<span data-ttu-id="7bad0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7bad0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7bad0-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="7bad0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7bad0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7bad0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7bad0-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="7bad0-110">Called by:</span></span>  <br/> |<span data-ttu-id="7bad0-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="7bad0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="7bad0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bad0-112">Parameters</span></span>

<span data-ttu-id="7bad0-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="7bad0-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="7bad0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bad0-114">Return value</span></span>

<span data-ttu-id="7bad0-115">Функция **MAPIGetDefaultMalloc** возвращает указатель на функцию выделения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bad0-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

