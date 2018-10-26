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
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578264"
---
# <a name="ftsubft"></a><span data-ttu-id="e7268-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="e7268-103">FtSubFt</span></span>

  
  
<span data-ttu-id="e7268-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7268-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7268-105">Вычитает один 64-разрядных целых чисел из другого.</span><span class="sxs-lookup"><span data-stu-id="e7268-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7268-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e7268-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7268-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e7268-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7268-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e7268-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7268-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7268-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7268-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e7268-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7268-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="e7268-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="e7268-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7268-112">Parameters</span></span>

 <span data-ttu-id="e7268-113">_Уменьшаемое_</span><span class="sxs-lookup"><span data-stu-id="e7268-113">_Minuend_</span></span>
  
> <span data-ttu-id="e7268-114">[in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия, из которой должна быть вычитается значение с помощью параметра _вычитаемое_ .</span><span class="sxs-lookup"><span data-stu-id="e7268-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="e7268-115">_Вычитаемое_</span><span class="sxs-lookup"><span data-stu-id="e7268-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="e7268-116">[in] Структура **FILETIME** , содержащую целых 64-разрядная версия, вычитается из значения, указанного параметром _Уменьшаемое_ .</span><span class="sxs-lookup"><span data-stu-id="e7268-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7268-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7268-117">Return value</span></span>

<span data-ttu-id="e7268-118">Функция **FtSubFt** возвращает структуру **FILETIME** , содержащую результат вычитания.</span><span class="sxs-lookup"><span data-stu-id="e7268-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="e7268-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="e7268-119">The two input parameters remain unchanged.</span></span> 
  

