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
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808417"
---
# <a name="fbadrestriction"></a><span data-ttu-id="b6624-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="b6624-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="b6624-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6624-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6624-105">Проверка ограничений, используются для ограничения представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b6624-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6624-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b6624-106">Header file:</span></span>  <br/> |<span data-ttu-id="b6624-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b6624-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b6624-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b6624-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b6624-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b6624-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b6624-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b6624-110">Called by:</span></span>  <br/> |<span data-ttu-id="b6624-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b6624-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="b6624-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6624-112">Parameters</span></span>

 <span data-ttu-id="b6624-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="b6624-113">_lpres_</span></span>
  
> <span data-ttu-id="b6624-114">[in] Структура [SRestriction](srestriction.md) , определение ограничения для проверки.</span><span class="sxs-lookup"><span data-stu-id="b6624-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b6624-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b6624-115">Return value</span></span>

<span data-ttu-id="b6624-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="b6624-116">TRUE</span></span> 
  
> <span data-ttu-id="b6624-117">Указанный ограничение, или одно или несколько его subrestrictions является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b6624-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="b6624-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6624-118">FALSE</span></span> 
  
> <span data-ttu-id="b6624-119">Указанный ограничение и все его subrestrictions являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="b6624-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6624-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="b6624-120">Remarks</span></span>

<span data-ttu-id="b6624-121">После проверки ограничения может быть передан в вызовы метода [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице, определенные строки, метод [IMAPITable::FindRow](imapitable-findrow.md) , найдите строку в таблице и методы [IMAPIContainer](imapicontainerimapiprop.md) интерфейс для выполнения ограничения для объекта-контейнера.</span><span class="sxs-lookup"><span data-stu-id="b6624-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

