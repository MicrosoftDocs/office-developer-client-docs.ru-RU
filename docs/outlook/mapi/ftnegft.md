---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808528"
---
# <a name="ftnegft"></a><span data-ttu-id="0d827-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="0d827-103">FtNegFt</span></span>

  
  
<span data-ttu-id="0d827-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d827-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d827-105">Вычисляет два элемента дополнения из 64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="0d827-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d827-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0d827-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d827-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0d827-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0d827-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0d827-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d827-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d827-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d827-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0d827-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d827-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="0d827-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="0d827-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d827-112">Parameters</span></span>

 <span data-ttu-id="0d827-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="0d827-113">_ft_</span></span>
  
> <span data-ttu-id="0d827-114">[in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, для которого нужно вычислить два элемента дополнения.</span><span class="sxs-lookup"><span data-stu-id="0d827-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d827-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0d827-115">Return value</span></span>

<span data-ttu-id="0d827-116">Функция **FtNegFt** возвращает структуру **FILETIME** , содержащую два элемента дополнения целого числа.</span><span class="sxs-lookup"><span data-stu-id="0d827-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="0d827-117">Входной параметр остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="0d827-117">The input parameter remains unchanged.</span></span> 
  

