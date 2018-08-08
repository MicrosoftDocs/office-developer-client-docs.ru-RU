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
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808425"
---
# <a name="fequalnames"></a><span data-ttu-id="15b4c-103">FEqualNames</span><span class="sxs-lookup"><span data-stu-id="15b4c-103">FEqualNames</span></span>

  
  
<span data-ttu-id="15b4c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15b4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15b4c-105">Определяет, одинаковы ли два MAPI с именем свойства.</span><span class="sxs-lookup"><span data-stu-id="15b4c-105">Determines whether two MAPI named properties are the same.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15b4c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="15b4c-106">Header file:</span></span>  <br/> |<span data-ttu-id="15b4c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="15b4c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="15b4c-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="15b4c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="15b4c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="15b4c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="15b4c-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="15b4c-110">Called by:</span></span>  <br/> |<span data-ttu-id="15b4c-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="15b4c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a><span data-ttu-id="15b4c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="15b4c-112">Parameters</span></span>

 <span data-ttu-id="15b4c-113">_lpName1_</span><span class="sxs-lookup"><span data-stu-id="15b4c-113">_lpName1_</span></span>
  
> <span data-ttu-id="15b4c-114">[in] Указатель на структуру [MAPINAMEID](mapinameid.md) , описывающий первый именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="15b4c-114">[in] Pointer to a [MAPINAMEID](mapinameid.md) structure describing the first named property.</span></span> 
    
 <span data-ttu-id="15b4c-115">_lpName2_</span><span class="sxs-lookup"><span data-stu-id="15b4c-115">_lpName2_</span></span>
  
> <span data-ttu-id="15b4c-116">[in] Указатель на структуру **MAPINAMEID** , описывающее второй именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="15b4c-116">[in] Pointer to a **MAPINAMEID** structure describing the second named property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="15b4c-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="15b4c-117">Return value</span></span>

<span data-ttu-id="15b4c-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="15b4c-118">TRUE</span></span> 
  
> <span data-ttu-id="15b4c-119">Имена двух свойство равны.</span><span class="sxs-lookup"><span data-stu-id="15b4c-119">The two property names are equal.</span></span> 
    
<span data-ttu-id="15b4c-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="15b4c-120">FALSE</span></span> 
  
> <span data-ttu-id="15b4c-121">Имена двух свойств не совпадают.</span><span class="sxs-lookup"><span data-stu-id="15b4c-121">The two property names are not equal.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15b4c-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="15b4c-122">Remarks</span></span>

<span data-ttu-id="15b4c-123">Функция **FEqualNames** полезен, так как структура **MAPINAMEID** содержит [идентификатор GUID](guid.md) и может представлять имя свойства в несколько способов.</span><span class="sxs-lookup"><span data-stu-id="15b4c-123">The **FEqualNames** function is useful because the **MAPINAMEID** structure contains a [GUID](guid.md) and can represent the property name itself in more than one way.</span></span> <span data-ttu-id="15b4c-124">Это означает, что две структуры нельзя сравнивать простой двоичные методами.</span><span class="sxs-lookup"><span data-stu-id="15b4c-124">This means the two structures cannot be compared by simple binary methods.</span></span> 
  
<span data-ttu-id="15b4c-125">Процесс тестирования задается с учетом регистра для строк имя свойства.</span><span class="sxs-lookup"><span data-stu-id="15b4c-125">The testing process is case-sensitive for the property name strings.</span></span> 
  

