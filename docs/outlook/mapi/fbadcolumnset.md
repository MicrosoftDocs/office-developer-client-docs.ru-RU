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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341008"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="6d8bc-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="6d8bc-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="6d8bc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d8bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d8bc-105">Проверяет допустимость набора столбцов таблицы для использования поставщиком услуг при следующем вызове метода [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="6d8bc-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d8bc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6d8bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="6d8bc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6d8bc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6d8bc-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6d8bc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6d8bc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8bc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6d8bc-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6d8bc-110">Called by:</span></span>  <br/> |<span data-ttu-id="6d8bc-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="6d8bc-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="6d8bc-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d8bc-112">Parameters</span></span>

 <span data-ttu-id="6d8bc-113">_Лпптаколс_</span><span class="sxs-lookup"><span data-stu-id="6d8bc-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="6d8bc-114">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, определяющих столбцы таблицы, которые необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="6d8bc-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6d8bc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d8bc-115">Return value</span></span>

<span data-ttu-id="6d8bc-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="6d8bc-116">TRUE</span></span> 
  
> <span data-ttu-id="6d8bc-117">Указан недопустимый набор столбцов.</span><span class="sxs-lookup"><span data-stu-id="6d8bc-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="6d8bc-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="6d8bc-118">FALSE</span></span> 
  
> <span data-ttu-id="6d8bc-119">Указанный набор столбцов является допустимым.</span><span class="sxs-lookup"><span data-stu-id="6d8bc-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d8bc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d8bc-120">Remarks</span></span>

<span data-ttu-id="6d8bc-121">Функция **фбадколумнсет** обрабатывает столбцы типа пт_еррор как недопустимые и столбцы типа пт_нулл как допустимые.</span><span class="sxs-lookup"><span data-stu-id="6d8bc-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

