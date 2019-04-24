---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340966"
---
# <a name="fbadrestriction"></a><span data-ttu-id="d8016-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="d8016-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="d8016-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8016-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8016-105">Проверяет ограничение, используемое для ограничения представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="d8016-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8016-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d8016-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8016-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d8016-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d8016-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d8016-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8016-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8016-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8016-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d8016-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8016-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d8016-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="d8016-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8016-112">Parameters</span></span>

 <span data-ttu-id="d8016-113">_лпрес_</span><span class="sxs-lookup"><span data-stu-id="d8016-113">_lpres_</span></span>
  
> <span data-ttu-id="d8016-114">возврата Структура [срестриктион](srestriction.md) , определяющая ограничение, которое необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="d8016-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8016-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8016-115">Return value</span></span>

<span data-ttu-id="d8016-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d8016-116">TRUE</span></span> 
  
> <span data-ttu-id="d8016-117">Указанное ограничение или один или несколько его подограничений являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="d8016-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="d8016-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d8016-118">FALSE</span></span> 
  
> <span data-ttu-id="d8016-119">Указанное ограничение и все его подограничения действительны.</span><span class="sxs-lookup"><span data-stu-id="d8016-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8016-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8016-120">Remarks</span></span>

<span data-ttu-id="d8016-121">После проверки ограничения его можно передать в вызовах метода [IMAPITable:: restrict](imapitable-restrict.md) , чтобы ограничить таблицу определенными строками, на метод [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения строки таблицы и для методов объекта [IMAPIContainer](imapicontainerimapiprop.md) интерфейс для выполнения ограничения для объекта Container.</span><span class="sxs-lookup"><span data-stu-id="d8016-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

