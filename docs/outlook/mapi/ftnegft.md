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
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589240"
---
# <a name="ftnegft"></a><span data-ttu-id="432cf-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="432cf-103">FtNegFt</span></span>

  
  
<span data-ttu-id="432cf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="432cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="432cf-105">Вычисляет два элемента дополнения из 64-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="432cf-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="432cf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="432cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="432cf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="432cf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="432cf-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="432cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="432cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="432cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="432cf-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="432cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="432cf-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="432cf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="432cf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="432cf-112">Parameters</span></span>

 <span data-ttu-id="432cf-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="432cf-113">_ft_</span></span>
  
> <span data-ttu-id="432cf-114">[in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, для которого нужно вычислить два элемента дополнения.</span><span class="sxs-lookup"><span data-stu-id="432cf-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="432cf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="432cf-115">Return value</span></span>

<span data-ttu-id="432cf-116">Функция **FtNegFt** возвращает структуру **FILETIME** , содержащую два элемента дополнения целого числа.</span><span class="sxs-lookup"><span data-stu-id="432cf-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="432cf-117">Входной параметр остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="432cf-117">The input parameter remains unchanged.</span></span> 
  

