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
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575100"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="62ce3-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="62ce3-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="62ce3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62ce3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62ce3-105">Тестов, задайте действия столбец таблицы для использования поставщиком услуг в последующих вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="62ce3-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62ce3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="62ce3-106">Header file:</span></span>  <br/> |<span data-ttu-id="62ce3-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="62ce3-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="62ce3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="62ce3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="62ce3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="62ce3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="62ce3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="62ce3-110">Called by:</span></span>  <br/> |<span data-ttu-id="62ce3-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="62ce3-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="62ce3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="62ce3-112">Parameters</span></span>

 <span data-ttu-id="62ce3-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="62ce3-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="62ce3-114">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, определение столбцов в таблице для проверки.</span><span class="sxs-lookup"><span data-stu-id="62ce3-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="62ce3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62ce3-115">Return value</span></span>

<span data-ttu-id="62ce3-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="62ce3-116">TRUE</span></span> 
  
> <span data-ttu-id="62ce3-117">Недопустимый набор указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="62ce3-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="62ce3-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="62ce3-118">FALSE</span></span> 
  
> <span data-ttu-id="62ce3-119">Набор указанного столбца является допустимым.</span><span class="sxs-lookup"><span data-stu-id="62ce3-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62ce3-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="62ce3-120">Remarks</span></span>

<span data-ttu-id="62ce3-121">Функция **FBadColumnSet** обрабатывает столбцы типа PT_ERROR как недопустимый и столбцы типа PT_NULL действительным.</span><span class="sxs-lookup"><span data-stu-id="62ce3-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

