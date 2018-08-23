---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2bfe2841592987c530f6323db94834c1dcb64b2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576640"
---
# <a name="ulpropsize"></a><span data-ttu-id="6aa53-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="6aa53-103">UlPropSize</span></span>

  
  
<span data-ttu-id="6aa53-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6aa53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6aa53-105">Возвращает размер значения одного свойства.</span><span class="sxs-lookup"><span data-stu-id="6aa53-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6aa53-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6aa53-106">Header file:</span></span>  <br/> |<span data-ttu-id="6aa53-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6aa53-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6aa53-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="6aa53-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6aa53-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6aa53-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6aa53-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="6aa53-110">Called by:</span></span>  <br/> |<span data-ttu-id="6aa53-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="6aa53-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="6aa53-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6aa53-112">Parameters</span></span>

 <span data-ttu-id="6aa53-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="6aa53-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="6aa53-114">[in] Указатель на структуру [SPropValue](spropvalue.md) определение свойства, которое должно быть измеряется.</span><span class="sxs-lookup"><span data-stu-id="6aa53-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6aa53-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6aa53-115">Return value</span></span>

<span data-ttu-id="6aa53-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6aa53-116">S_OK</span></span> 
  
> <span data-ttu-id="6aa53-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6aa53-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6aa53-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6aa53-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="6aa53-119">Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="6aa53-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6aa53-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="6aa53-120">Remarks</span></span>

<span data-ttu-id="6aa53-121">Функция **UlPropSize** возвращает размер, в байтах, значение свойства для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="6aa53-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="6aa53-122">Она игнорирует размер в оставшейся части структуры **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="6aa53-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

