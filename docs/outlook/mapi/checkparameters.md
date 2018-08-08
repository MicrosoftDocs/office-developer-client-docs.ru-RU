---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a693c06d933c7e93d384aac8da8d5311eaf1d9da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808192"
---
# <a name="checkparameters"></a><span data-ttu-id="388fd-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="388fd-103">CheckParameters</span></span>

  
  
<span data-ttu-id="388fd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="388fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="388fd-105">Вызывает внутренней функции для проверки параметров отладки на методы поставщика службы вызывается MAPI.</span><span class="sxs-lookup"><span data-stu-id="388fd-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="388fd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="388fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="388fd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="388fd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="388fd-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="388fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="388fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="388fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="388fd-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="388fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="388fd-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="388fd-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="388fd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="388fd-112">Parameters</span></span>

 <span data-ttu-id="388fd-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="388fd-113">_eMethod_</span></span>
  
> <span data-ttu-id="388fd-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="388fd-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="388fd-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="388fd-115">_First_</span></span>
  
> <span data-ttu-id="388fd-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="388fd-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="388fd-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="388fd-117">Return value</span></span>

<span data-ttu-id="388fd-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="388fd-118">S_OK</span></span> 
  
> <span data-ttu-id="388fd-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="388fd-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="388fd-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="388fd-120">Remarks</span></span>

<span data-ttu-id="388fd-121">Макрос **CheckParameters** был заменен макрос [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="388fd-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="388fd-122">**CheckParms** рекомендуется для всех платформ.</span><span class="sxs-lookup"><span data-stu-id="388fd-122">**CheckParms** is recommended on all platforms.</span></span> 
  

