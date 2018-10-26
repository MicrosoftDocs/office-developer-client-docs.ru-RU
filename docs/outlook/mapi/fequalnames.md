---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570851"
---
# <a name="fequalnames"></a><span data-ttu-id="a3974-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="a3974-103">FEqualNames</span></span>

  
  
<span data-ttu-id="a3974-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3974-105">Определяет, одинаковы ли два MAPI с именем свойства.</span><span class="sxs-lookup"><span data-stu-id="a3974-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3974-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a3974-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3974-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a3974-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3974-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a3974-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3974-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3974-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3974-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a3974-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3974-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="a3974-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="a3974-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3974-112">Parameters</span></span>

 <span data-ttu-id="a3974-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="a3974-113">_lpName1_</span></span>
  
> <span data-ttu-id="a3974-114">[in] Указатель на структуру [MAPINAMEID](mapinameid.md) , описывающий первый именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="a3974-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="a3974-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="a3974-115">_lpName2_</span></span>
  
> <span data-ttu-id="a3974-116">[in] Указатель на структуру **MAPINAMEID** , описывающее второй именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="a3974-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3974-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3974-117">Return value</span></span>

<span data-ttu-id="a3974-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="a3974-118">TRUE</span></span> 
  
> <span data-ttu-id="a3974-119">Имена двух свойство равны.</span><span class="sxs-lookup"><span data-stu-id="a3974-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="a3974-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="a3974-120">FALSE</span></span> 
  
> <span data-ttu-id="a3974-121">Имена двух свойств не совпадают.</span><span class="sxs-lookup"><span data-stu-id="a3974-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3974-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3974-122">Remarks</span></span>

<span data-ttu-id="a3974-123">Функция **FEqualNames** полезен, так как структура **MAPINAMEID** содержит [идентификатор GUID](guid.md) и может представлять имя свойства в несколько способов.</span><span class="sxs-lookup"><span data-stu-id="a3974-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="a3974-124">Это означает, что две структуры нельзя сравнивать простой двоичные методами.</span><span class="sxs-lookup"><span data-stu-id="a3974-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="a3974-125">Процесс тестирования задается с учетом регистра для строк имя свойства.</span><span class="sxs-lookup"><span data-stu-id="a3974-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

