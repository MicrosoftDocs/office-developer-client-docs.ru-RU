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
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809867"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="66074-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="66074-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="66074-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66074-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66074-105">Получает адрес функции выделения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66074-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66074-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="66074-106">Header file:</span></span>  <br/> |<span data-ttu-id="66074-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="66074-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="66074-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="66074-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="66074-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="66074-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="66074-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="66074-110">Called by:</span></span>  <br/> |<span data-ttu-id="66074-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="66074-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="66074-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="66074-112">Parameters</span></span>

<span data-ttu-id="66074-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="66074-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="66074-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66074-114">Return value</span></span>

<span data-ttu-id="66074-115">Функция **MAPIGetDefaultMalloc** возвращает указатель на функцию выделения памяти MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66074-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

