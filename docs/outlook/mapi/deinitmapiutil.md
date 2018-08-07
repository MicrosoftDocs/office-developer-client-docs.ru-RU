---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808259"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="31289-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="31289-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="31289-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31289-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31289-105">Освобождает служебной программы функций, вызываемых явным образом с помощью функции [ScInitMapiUtil](scinitmapiutil.md) или неявно с помощью функции [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="31289-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31289-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="31289-106">Header file:</span></span>  <br/> |<span data-ttu-id="31289-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="31289-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="31289-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="31289-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31289-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31289-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31289-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="31289-110">Called by:</span></span>  <br/> |<span data-ttu-id="31289-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="31289-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="31289-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="31289-112">Parameters</span></span>

<span data-ttu-id="31289-113">Нет</span><span class="sxs-lookup"><span data-stu-id="31289-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="31289-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="31289-115">Нет</span><span class="sxs-lookup"><span data-stu-id="31289-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="31289-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="31289-116">Remarks</span></span>

<span data-ttu-id="31289-117">Функция **DeinitMapiUtil** release функции инициализации с [ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="31289-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="31289-118">По завершении работы функций, вызываемых **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их.</span><span class="sxs-lookup"><span data-stu-id="31289-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="31289-119">С другой стороны [MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="31289-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

