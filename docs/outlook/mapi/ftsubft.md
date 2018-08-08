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
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808523"
---
# <a name="ftsubft"></a><span data-ttu-id="eef4e-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="eef4e-103">FtSubFt</span></span>

  
  
<span data-ttu-id="eef4e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eef4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eef4e-105">Вычитает один 64-разрядных целых чисел из другого.</span><span class="sxs-lookup"><span data-stu-id="eef4e-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eef4e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="eef4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="eef4e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="eef4e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="eef4e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="eef4e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eef4e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eef4e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eef4e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="eef4e-110">Called by:</span></span>  <br/> |<span data-ttu-id="eef4e-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="eef4e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="eef4e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="eef4e-112">Parameters</span></span>

 <span data-ttu-id="eef4e-113">_Уменьшаемое_</span><span class="sxs-lookup"><span data-stu-id="eef4e-113">_Minuend_</span></span>
  
> <span data-ttu-id="eef4e-114">[in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, из которой должна быть вычитается значение с помощью параметра _вычитаемое_ .</span><span class="sxs-lookup"><span data-stu-id="eef4e-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="eef4e-115">_Вычитаемое_</span><span class="sxs-lookup"><span data-stu-id="eef4e-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="eef4e-116">[in] Структура **FILETIME** , содержащую целых 64-разрядная версия, вычитается из значения, указанного параметром _Уменьшаемое_ .</span><span class="sxs-lookup"><span data-stu-id="eef4e-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eef4e-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="eef4e-117">Return value</span></span>

<span data-ttu-id="eef4e-118">Функция **FtSubFt** возвращает структуру **FILETIME** , содержащую результат вычитания.</span><span class="sxs-lookup"><span data-stu-id="eef4e-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="eef4e-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="eef4e-119">The two input parameters remain unchanged.</span></span> 
  

