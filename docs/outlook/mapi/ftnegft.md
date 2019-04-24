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
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327974"
---
# <a name="ftnegft"></a><span data-ttu-id="cd1d4-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="cd1d4-103">FtNegFt</span></span>

  
  
<span data-ttu-id="cd1d4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd1d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd1d4-105">Вычисляет дополнение для двух неподписанного 64 — разрядного целого числа.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd1d4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cd1d4-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd1d4-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="cd1d4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cd1d4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cd1d4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd1d4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cd1d4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cd1d4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cd1d4-110">Called by:</span></span>  <br/> |<span data-ttu-id="cd1d4-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="cd1d4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="cd1d4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd1d4-112">Parameters</span></span>

 <span data-ttu-id="cd1d4-113">_метр_</span><span class="sxs-lookup"><span data-stu-id="cd1d4-113">_ft_</span></span>
  
> <span data-ttu-id="cd1d4-114">возврата Структура [fileTime](filetime.md) , которая содержит неподписанное 64 — разрядное целое число, для которого вычисляется дополнение к двум.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cd1d4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd1d4-115">Return value</span></span>

<span data-ttu-id="cd1d4-116">Функция **фтнегфт** возвращает структуру **fileTime** , которая содержит дополнение до двух элементов целого числа.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="cd1d4-117">Входной параметр остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-117">The input parameter remains unchanged.</span></span> 
  

