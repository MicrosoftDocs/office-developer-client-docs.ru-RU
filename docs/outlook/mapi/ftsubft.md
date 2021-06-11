---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408420"
---
# <a name="ftsubft"></a><span data-ttu-id="0aea3-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="0aea3-103">FtSubFt</span></span>

  
  
<span data-ttu-id="0aea3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aea3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aea3-105">Вычитает один неподписаный 64-битный шестерка из другого.</span><span class="sxs-lookup"><span data-stu-id="0aea3-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0aea3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0aea3-106">Header file:</span></span>  <br/> |<span data-ttu-id="0aea3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0aea3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0aea3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0aea3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0aea3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0aea3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0aea3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0aea3-110">Called by:</span></span>  <br/> |<span data-ttu-id="0aea3-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0aea3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="0aea3-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0aea3-112">Parameters</span></span>

 <span data-ttu-id="0aea3-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="0aea3-113">_Minuend_</span></span>
  
> <span data-ttu-id="0aea3-114">[in] Структура [FILETIME,](filetime.md) которая содержит неподписаный 64-битный набор, из которого должно быть вычитано значение в параметре _Subtrahend._</span><span class="sxs-lookup"><span data-stu-id="0aea3-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="0aea3-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="0aea3-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="0aea3-116">[in] Структура **FILETIME** с неподписаным 64-битным набором, вычитаемой из значения, указываемого параметром _Minuend._</span><span class="sxs-lookup"><span data-stu-id="0aea3-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0aea3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aea3-117">Return value</span></span>

<span data-ttu-id="0aea3-118">Функция **FTSubFt** возвращает структуру **FILETIME,** которая содержит результат вычитания.</span><span class="sxs-lookup"><span data-stu-id="0aea3-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="0aea3-119">Два параметра ввода остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="0aea3-119">The two input parameters remain unchanged.</span></span> 
  

