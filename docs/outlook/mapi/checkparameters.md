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
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332079"
---
# <a name="checkparameters"></a><span data-ttu-id="ac870-103">CheckParameters</span><span class="sxs-lookup"><span data-stu-id="ac870-103">CheckParameters</span></span>

  
  
<span data-ttu-id="ac870-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac870-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac870-105">Вызывает внутреннюю функцию для проверки параметров отладки методов поставщика услуг, вызываемых MAPI.</span><span class="sxs-lookup"><span data-stu-id="ac870-105">Calls an internal function to validate debugging parameters on service provider methods called by MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac870-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ac870-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac870-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="ac870-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="ac870-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ac870-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ac870-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ac870-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ac870-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ac870-110">Called by:</span></span>  <br/> |<span data-ttu-id="ac870-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ac870-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="ac870-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac870-112">Parameters</span></span>

 <span data-ttu-id="ac870-113">_Емесод_</span><span class="sxs-lookup"><span data-stu-id="ac870-113">_eMethod_</span></span>
  
> <span data-ttu-id="ac870-114">возврата Определяет, по перечислению, метод, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="ac870-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="ac870-115">_First_</span><span class="sxs-lookup"><span data-stu-id="ac870-115">_First_</span></span>
  
> <span data-ttu-id="ac870-116">возврата Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="ac870-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac870-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac870-117">Return value</span></span>

<span data-ttu-id="ac870-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac870-118">S_OK</span></span> 
  
> <span data-ttu-id="ac870-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ac870-119">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac870-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac870-120">Remarks</span></span>

<span data-ttu-id="ac870-121">Макрос **чеккпараметерс** был заменен макросом [чеккпармс](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="ac870-121">The **CheckParameters** macro has been superseded by the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="ac870-122">**Чеккпармс** рекомендуется использовать на всех платформах.</span><span class="sxs-lookup"><span data-stu-id="ac870-122">**CheckParms** is recommended on all platforms.</span></span> 
  

