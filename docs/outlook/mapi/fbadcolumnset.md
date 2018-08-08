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
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808420"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="ea0c7-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="ea0c7-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="ea0c7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea0c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea0c7-105">Тестов, задайте действия столбец таблицы для использования поставщиком услуг в последующих вызов метода [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="ea0c7-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea0c7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ea0c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea0c7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ea0c7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ea0c7-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="ea0c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ea0c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ea0c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ea0c7-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ea0c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="ea0c7-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ea0c7-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="ea0c7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea0c7-112">Parameters</span></span>

 <span data-ttu-id="ea0c7-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="ea0c7-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="ea0c7-114">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, определение столбцов в таблице для проверки.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ea0c7-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="ea0c7-115">Return value</span></span>

<span data-ttu-id="ea0c7-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="ea0c7-116">TRUE</span></span> 
  
> <span data-ttu-id="ea0c7-117">Недопустимый набор указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="ea0c7-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="ea0c7-118">FALSE</span></span> 
  
> <span data-ttu-id="ea0c7-119">Набор указанного столбца является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea0c7-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="ea0c7-120">Remarks</span></span>

<span data-ttu-id="ea0c7-121">Функция **FBadColumnSet** обрабатывает столбцы типа PT_ERROR как недопустимый и столбцы типа PT_NULL действительным.</span><span class="sxs-lookup"><span data-stu-id="ea0c7-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

