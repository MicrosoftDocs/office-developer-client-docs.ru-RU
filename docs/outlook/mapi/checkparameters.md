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
ms.openlocfilehash: f01d0ad7e7e6b1ad7a5e4c4838bb46ca143e0968
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567057"
---
# <a name="checkparameters"></a><span data-ttu-id="671ae-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="671ae-103">CheckParameters</span></span>

  
  
<span data-ttu-id="671ae-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="671ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="671ae-105">Вызывает внутренней функции для проверки параметров отладки на методы поставщика службы вызывается MAPI.</span><span class="sxs-lookup"><span data-stu-id="671ae-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="671ae-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="671ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="671ae-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="671ae-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="671ae-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="671ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="671ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="671ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="671ae-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="671ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="671ae-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="671ae-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="671ae-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="671ae-112">Parameters</span></span>

 <span data-ttu-id="671ae-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="671ae-113">_eMethod_</span></span>
  
> <span data-ttu-id="671ae-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="671ae-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="671ae-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="671ae-115">_First_</span></span>
  
> <span data-ttu-id="671ae-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="671ae-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="671ae-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="671ae-117">Return value</span></span>

<span data-ttu-id="671ae-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="671ae-118">S_OK</span></span> 
  
> <span data-ttu-id="671ae-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="671ae-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="671ae-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="671ae-120">Remarks</span></span>

<span data-ttu-id="671ae-121">Макрос **CheckParameters** был заменен макрос [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="671ae-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="671ae-122">**CheckParms** рекомендуется для всех платформ.</span><span class="sxs-lookup"><span data-stu-id="671ae-122">**CheckParms** is recommended on all platforms.</span></span> 
  

