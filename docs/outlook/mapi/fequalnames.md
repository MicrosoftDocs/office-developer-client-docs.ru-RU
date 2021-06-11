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
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414804"
---
# <a name="fequalnames"></a><span data-ttu-id="ecb07-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="ecb07-103">FEqualNames</span></span>

  
  
<span data-ttu-id="ecb07-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb07-105">Определяет, являются ли два свойства MAPI одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="ecb07-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecb07-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ecb07-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecb07-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ecb07-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ecb07-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ecb07-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ecb07-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ecb07-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ecb07-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ecb07-110">Called by:</span></span>  <br/> |<span data-ttu-id="ecb07-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ecb07-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="ecb07-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ecb07-112">Parameters</span></span>

 <span data-ttu-id="ecb07-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="ecb07-113">_lpName1_</span></span>
  
> <span data-ttu-id="ecb07-114">[in] Указатель на [структуру MAPINAMEID](mapinameid.md) с описанием первого имени свойства.</span><span class="sxs-lookup"><span data-stu-id="ecb07-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="ecb07-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="ecb07-115">_lpName2_</span></span>
  
> <span data-ttu-id="ecb07-116">[in] Указатель на **структуру MAPINAMEID** с описанием второго имени свойства.</span><span class="sxs-lookup"><span data-stu-id="ecb07-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ecb07-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecb07-117">Return value</span></span>

<span data-ttu-id="ecb07-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="ecb07-118">TRUE</span></span> 
  
> <span data-ttu-id="ecb07-119">Два имени свойств равны.</span><span class="sxs-lookup"><span data-stu-id="ecb07-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="ecb07-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="ecb07-120">FALSE</span></span> 
  
> <span data-ttu-id="ecb07-121">Два имени свойств не являются равными.</span><span class="sxs-lookup"><span data-stu-id="ecb07-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ecb07-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecb07-122">Remarks</span></span>

<span data-ttu-id="ecb07-123">Функция **FEqualNames** полезна, так как структура **MAPINAMEID** содержит [GUID](guid.md) и может представлять само имя свойства несколько способов.</span><span class="sxs-lookup"><span data-stu-id="ecb07-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="ecb07-124">Это означает, что две структуры нельзя сравнивать простыми двоичными методами.</span><span class="sxs-lookup"><span data-stu-id="ecb07-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="ecb07-125">Процесс тестирования является конфиденциальным для строк имени свойства.</span><span class="sxs-lookup"><span data-stu-id="ecb07-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

