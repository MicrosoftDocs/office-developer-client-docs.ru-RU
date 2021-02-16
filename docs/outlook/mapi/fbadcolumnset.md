---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434720"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="10074-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="10074-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="10074-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10074-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10074-105">Проверяет правильность набора столбцов таблицы для использования поставщиком службы при последующем вызове метода [IMAPITable::SetColumns.](imapitable-setcolumns.md)</span><span class="sxs-lookup"><span data-stu-id="10074-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10074-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="10074-106">Header file:</span></span>  <br/> |<span data-ttu-id="10074-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="10074-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="10074-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="10074-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="10074-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="10074-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="10074-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="10074-110">Called by:</span></span>  <br/> |<span data-ttu-id="10074-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="10074-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="10074-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="10074-112">Parameters</span></span>

 <span data-ttu-id="10074-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="10074-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="10074-114">[in] Указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, определяющих столбцы таблицы для проверки.</span><span class="sxs-lookup"><span data-stu-id="10074-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="10074-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10074-115">Return value</span></span>

<span data-ttu-id="10074-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="10074-116">TRUE</span></span> 
  
> <span data-ttu-id="10074-117">Указанный набор столбцов недействителен.</span><span class="sxs-lookup"><span data-stu-id="10074-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="10074-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="10074-118">FALSE</span></span> 
  
> <span data-ttu-id="10074-119">Указанный набор столбцов является допустимым.</span><span class="sxs-lookup"><span data-stu-id="10074-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10074-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="10074-120">Remarks</span></span>

<span data-ttu-id="10074-121">Функция **FBadColumnSet** обрабатывает столбцы типа PT_ERROR как недопустимые, а столбцы типа PT_NULL как допустимые.</span><span class="sxs-lookup"><span data-stu-id="10074-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

