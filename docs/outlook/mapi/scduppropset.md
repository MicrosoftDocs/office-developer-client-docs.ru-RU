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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351270"
---
# <a name="scduppropset"></a><span data-ttu-id="bc706-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="bc706-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="bc706-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc706-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc706-105">Дублирует массив значений свойства в отдельном блоке памяти MAPI, сочетая операции функций [сккопипропс](sccopyprops.md) и [сккаунтпропс](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="bc706-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc706-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bc706-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc706-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="bc706-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bc706-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="bc706-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc706-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bc706-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bc706-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="bc706-110">Called by:</span></span>  <br/> |<span data-ttu-id="bc706-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="bc706-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="bc706-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc706-112">Parameters</span></span>

 <span data-ttu-id="bc706-113">_кпроп_</span><span class="sxs-lookup"><span data-stu-id="bc706-113">_cprop_</span></span>
  
> <span data-ttu-id="bc706-114">возврата Количество значений свойств в массиве, указанном с помощью параметра _ргпроп_ .</span><span class="sxs-lookup"><span data-stu-id="bc706-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="bc706-115">_ргпроп_</span><span class="sxs-lookup"><span data-stu-id="bc706-115">_rgprop_</span></span>
  
> <span data-ttu-id="bc706-116">возврата Указатель на массив структур [спропвалуе](spropvalue.md) , определяющий значения свойств, которые должны дублироваться.</span><span class="sxs-lookup"><span data-stu-id="bc706-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="bc706-117">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="bc706-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="bc706-118">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти для дублированного массива.</span><span class="sxs-lookup"><span data-stu-id="bc706-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="bc706-119">_пргпроп_</span><span class="sxs-lookup"><span data-stu-id="bc706-119">_prgprop_</span></span>
  
> <span data-ttu-id="bc706-120">вышли Указатель на начальную позицию в памяти, в которой хранится возвращенный повторяющийся массив структур **спропвалуе** .</span><span class="sxs-lookup"><span data-stu-id="bc706-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bc706-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc706-121">Return value</span></span>

<span data-ttu-id="bc706-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc706-122">S_OK</span></span> 
  
> <span data-ttu-id="bc706-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bc706-123">The call succeeded and has returned the expected value or values.</span></span>
    

