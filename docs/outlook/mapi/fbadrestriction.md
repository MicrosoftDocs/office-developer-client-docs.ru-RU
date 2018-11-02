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
ms.openlocfilehash: 3d729e2a12ee19ee3aa4ded71263697eb739f154
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566308"
---
# <a name="fbadrestriction"></a><span data-ttu-id="e8b50-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="e8b50-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="e8b50-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8b50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8b50-105">Проверка ограничений, используются для ограничения представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="e8b50-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8b50-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e8b50-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8b50-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="e8b50-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="e8b50-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e8b50-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e8b50-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e8b50-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e8b50-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e8b50-110">Called by:</span></span>  <br/> |<span data-ttu-id="e8b50-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="e8b50-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="e8b50-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8b50-112">Parameters</span></span>

 <span data-ttu-id="e8b50-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="e8b50-113">_lpres_</span></span>
  
> <span data-ttu-id="e8b50-114">[in] Структура [SRestriction](srestriction.md) , определение ограничения для проверки.</span><span class="sxs-lookup"><span data-stu-id="e8b50-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8b50-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8b50-115">Return value</span></span>

<span data-ttu-id="e8b50-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="e8b50-116">TRUE</span></span> 
  
> <span data-ttu-id="e8b50-117">Указанный ограничение, или одно или несколько его subrestrictions является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="e8b50-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="e8b50-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8b50-118">FALSE</span></span> 
  
> <span data-ttu-id="e8b50-119">Указанный ограничение и все его subrestrictions являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="e8b50-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8b50-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8b50-120">Remarks</span></span>

<span data-ttu-id="e8b50-121">После проверки ограничения может быть передан в вызовы метода [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице, определенные строки, метод [IMAPITable::FindRow](imapitable-findrow.md) , найдите строку в таблице и методы [IMAPIContainer](imapicontainerimapiprop.md) интерфейс для выполнения ограничения для объекта-контейнера.</span><span class="sxs-lookup"><span data-stu-id="e8b50-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

