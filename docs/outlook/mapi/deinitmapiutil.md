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
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574799"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="8c388-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="8c388-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="8c388-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c388-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c388-105">Освобождает служебной программы функций, вызываемых явным образом с помощью функции [ScInitMapiUtil](scinitmapiutil.md) или неявно с помощью функции [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="8c388-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c388-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8c388-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c388-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8c388-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8c388-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="8c388-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c388-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8c388-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8c388-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="8c388-110">Called by:</span></span>  <br/> |<span data-ttu-id="8c388-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8c388-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="8c388-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c388-112">Parameters</span></span>

<span data-ttu-id="8c388-113">None</span><span class="sxs-lookup"><span data-stu-id="8c388-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="8c388-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8c388-114">Return value</span></span>

<span data-ttu-id="8c388-115">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8c388-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8c388-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c388-116">Remarks</span></span>

<span data-ttu-id="8c388-117">Функция **DeinitMapiUtil** release функции инициализации с [ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="8c388-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="8c388-118">По завершении работы функций, вызываемых **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их.</span><span class="sxs-lookup"><span data-stu-id="8c388-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="8c388-119">С другой стороны [MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="8c388-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

