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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336843"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="c35ab-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="c35ab-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="c35ab-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c35ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c35ab-105">Освобождает функции служебных программ, которые вызываются явно функцией [сЦинитмапиутил](scinitmapiutil.md) , или неявно функцией [мапиинитиализе](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="c35ab-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c35ab-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c35ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="c35ab-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="c35ab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c35ab-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c35ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c35ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c35ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c35ab-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c35ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="c35ab-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="c35ab-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="c35ab-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c35ab-112">Parameters</span></span>

<span data-ttu-id="c35ab-113">Нет</span><span class="sxs-lookup"><span data-stu-id="c35ab-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="c35ab-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c35ab-114">Return value</span></span>

<span data-ttu-id="c35ab-115">Нет</span><span class="sxs-lookup"><span data-stu-id="c35ab-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c35ab-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c35ab-116">Remarks</span></span>

<span data-ttu-id="c35ab-117">Функции выпуска функции **деинитмапиутил** , инициализированные с помощью [сЦинитмапиутил](scinitmapiutil.md) или [мапиинитиализе](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="c35ab-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="c35ab-118">При завершении использования функций, вызываемых **сЦинитмапиутил** , **деинитмапиутил** необходимо явно вызывать, чтобы освободить их.</span><span class="sxs-lookup"><span data-stu-id="c35ab-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="c35ab-119">В отличие от этого, [мапиунинитиализе](mapiuninitialize.md) неявно вызывает **деинитмапиутил**.</span><span class="sxs-lookup"><span data-stu-id="c35ab-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

