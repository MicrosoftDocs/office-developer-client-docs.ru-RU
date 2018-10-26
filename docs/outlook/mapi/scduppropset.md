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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581981"
---
# <a name="scduppropset"></a><span data-ttu-id="96392-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="96392-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="96392-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96392-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96392-105">Дублирует массива значение свойства в один блок памяти MAPI, объединяя операции функции [ScCopyProps](sccopyprops.md) и [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="96392-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96392-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="96392-106">Header file:</span></span>  <br/> |<span data-ttu-id="96392-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="96392-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="96392-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="96392-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="96392-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96392-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96392-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="96392-110">Called by:</span></span>  <br/> |<span data-ttu-id="96392-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="96392-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="96392-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="96392-112">Parameters</span></span>

 <span data-ttu-id="96392-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="96392-113">_cprop_</span></span>
  
> <span data-ttu-id="96392-114">[in] Число значений свойств в массива, указанного в параметре _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="96392-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="96392-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="96392-115">_rgprop_</span></span>
  
> <span data-ttu-id="96392-116">[in] Указатель на массив структур [SPropValue](spropvalue.md) определение значения свойств дублирование.</span><span class="sxs-lookup"><span data-stu-id="96392-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="96392-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="96392-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="96392-118">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти для повторяющихся массива.</span><span class="sxs-lookup"><span data-stu-id="96392-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="96392-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="96392-119">_prgprop_</span></span>
  
> <span data-ttu-id="96392-120">[out] Указатель на начальное положение в памяти хранения дублируемые возвращенный массив структур **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="96392-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="96392-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96392-121">Return value</span></span>

<span data-ttu-id="96392-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="96392-122">S_OK</span></span> 
  
> <span data-ttu-id="96392-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="96392-123">The call succeeded and has returned the expected value or values.</span></span>
    

