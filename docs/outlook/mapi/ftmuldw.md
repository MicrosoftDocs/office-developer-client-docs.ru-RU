---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406348"
---
# <a name="ftmuldw"></a><span data-ttu-id="80fd3-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="80fd3-103">FtMulDw</span></span>

  
  
<span data-ttu-id="80fd3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80fd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80fd3-105">Умножает неподписаное 64-битное 64-битное на неподписаное 32-битное.</span><span class="sxs-lookup"><span data-stu-id="80fd3-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80fd3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="80fd3-106">Header file:</span></span>  <br/> |<span data-ttu-id="80fd3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="80fd3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="80fd3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="80fd3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="80fd3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="80fd3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="80fd3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="80fd3-110">Called by:</span></span>  <br/> |<span data-ttu-id="80fd3-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="80fd3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="80fd3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="80fd3-112">Parameters</span></span>

 <span data-ttu-id="80fd3-113">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="80fd3-113">_Multiplier_</span></span>
  
> <span data-ttu-id="80fd3-114">[in] Двойное слово, которое содержит 32-разрядный множитель неподписаных 32-разрядных номеров.</span><span class="sxs-lookup"><span data-stu-id="80fd3-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="80fd3-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="80fd3-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="80fd3-116">[in] Структура [FILETIME,](filetime.md) которая содержит неподписаенное 64-битное 64-битное значение, умноженное на значение параметра _Multiplier._</span><span class="sxs-lookup"><span data-stu-id="80fd3-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="80fd3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80fd3-117">Return value</span></span>

<span data-ttu-id="80fd3-118">Функция **FtMulDw** возвращает структуру **FILETIME,** которая содержит продукт двух integers.</span><span class="sxs-lookup"><span data-stu-id="80fd3-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="80fd3-119">Два входных параметра остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="80fd3-119">The two input parameters remain unchanged.</span></span> 
  

