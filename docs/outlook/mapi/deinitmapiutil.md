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
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427348"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="32002-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="32002-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="32002-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32002-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32002-105">Освобождает функции, явным образом называемые [функцией ScInitMapiUtil](scinitmapiutil.md) или неявно [функцией MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="32002-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32002-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="32002-106">Header file:</span></span>  <br/> |<span data-ttu-id="32002-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="32002-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="32002-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="32002-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="32002-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="32002-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="32002-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="32002-110">Called by:</span></span>  <br/> |<span data-ttu-id="32002-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="32002-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="32002-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="32002-112">Parameters</span></span>

<span data-ttu-id="32002-113">Нет</span><span class="sxs-lookup"><span data-stu-id="32002-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="32002-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32002-114">Return value</span></span>

<span data-ttu-id="32002-115">Нет</span><span class="sxs-lookup"><span data-stu-id="32002-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32002-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="32002-116">Remarks</span></span>

<span data-ttu-id="32002-117">Функции **выпуска функции DeinitMapiUtil,** инициализированные с [помощью ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="32002-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="32002-118">После завершения использования функций, называемых **ScInitMapiUtil,** необходимо явным образом с помощью **deinitMapiUtil** освободить их.</span><span class="sxs-lookup"><span data-stu-id="32002-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="32002-119">С другой [стороны, MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil.**</span><span class="sxs-lookup"><span data-stu-id="32002-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

