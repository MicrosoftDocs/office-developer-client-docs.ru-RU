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
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416904"
---
# <a name="ulpropsize"></a><span data-ttu-id="b4330-103">UlPropSize</span><span class="sxs-lookup"><span data-stu-id="b4330-103">UlPropSize</span></span>

  
  
<span data-ttu-id="b4330-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4330-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4330-105">Возвращает размер одного значения свойства.</span><span class="sxs-lookup"><span data-stu-id="b4330-105">Returns the size of a single property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4330-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b4330-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4330-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4330-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b4330-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b4330-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4330-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b4330-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b4330-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b4330-110">Called by:</span></span>  <br/> |<span data-ttu-id="b4330-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b4330-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="b4330-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4330-112">Parameters</span></span>

 <span data-ttu-id="b4330-113">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="b4330-113">_lpSPropValue_</span></span>
  
> <span data-ttu-id="b4330-114">[in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей измеримое свойство.</span><span class="sxs-lookup"><span data-stu-id="b4330-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property to be measured.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4330-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4330-115">Return value</span></span>

<span data-ttu-id="b4330-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4330-116">S_OK</span></span> 
  
> <span data-ttu-id="b4330-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b4330-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b4330-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b4330-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b4330-119">Ошибка непредвиденного или неизвестного источника помешала выполнению операции.</span><span class="sxs-lookup"><span data-stu-id="b4330-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4330-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4330-120">Remarks</span></span>

<span data-ttu-id="b4330-121">Функция **UlPropSize** возвращает размер значения свойства для указанного свойства (в bytes).</span><span class="sxs-lookup"><span data-stu-id="b4330-121">The **UlPropSize** function returns the size, in bytes, of the property value for the specified property.</span></span> <span data-ttu-id="b4330-122">Он игнорирует размер оставшейся части **структуры SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="b4330-122">It disregards the size of the remainder of the **SPropValue** structure.</span></span> 
  

