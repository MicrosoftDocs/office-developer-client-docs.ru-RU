---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406019"
---
# <a name="scduppropset"></a><span data-ttu-id="93f47-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="93f47-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="93f47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93f47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93f47-105">Дублирует массив значений свойств в одном блоке памяти MAPI, сочетающий операции функций [ScCopyProps](sccopyprops.md) и [ScCountProps.](sccountprops.md)</span><span class="sxs-lookup"><span data-stu-id="93f47-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93f47-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="93f47-106">Header file:</span></span>  <br/> |<span data-ttu-id="93f47-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="93f47-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="93f47-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="93f47-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93f47-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93f47-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93f47-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="93f47-110">Called by:</span></span>  <br/> |<span data-ttu-id="93f47-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="93f47-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="93f47-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="93f47-112">Parameters</span></span>

 <span data-ttu-id="93f47-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="93f47-113">_cprop_</span></span>
  
> <span data-ttu-id="93f47-114">[in] Количество значений свойств в массиве, указанных _параметром rgprop._</span><span class="sxs-lookup"><span data-stu-id="93f47-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="93f47-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="93f47-115">_rgprop_</span></span>
  
> <span data-ttu-id="93f47-116">[in] Указатель на массив [структур SPropValue,](spropvalue.md) определяющих повторяющиеся значения свойств.</span><span class="sxs-lookup"><span data-stu-id="93f47-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="93f47-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="93f47-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="93f47-118">[in] Указатель на функцию [MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти для дубликатного массива.</span><span class="sxs-lookup"><span data-stu-id="93f47-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="93f47-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="93f47-119">_prgprop_</span></span>
  
> <span data-ttu-id="93f47-120">[вышел] Указатель на исходное положение в памяти, где хранится возвращаемая дублированная массива структур **SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="93f47-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93f47-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93f47-121">Return value</span></span>

<span data-ttu-id="93f47-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="93f47-122">S_OK</span></span> 
  
> <span data-ttu-id="93f47-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="93f47-123">The call succeeded and has returned the expected value or values.</span></span>
    

