---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 750d8b8d50acb9cf7340e6553062412667398665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812070"
---
# <a name="propcopymore"></a><span data-ttu-id="c0b6e-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="c0b6e-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="c0b6e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0b6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0b6e-105">Копирует значения одного свойства из исходного расположения в месте назначения.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0b6e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c0b6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0b6e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c0b6e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c0b6e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c0b6e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0b6e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0b6e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0b6e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c0b6e-110">Called by:</span></span>  <br/> |<span data-ttu-id="c0b6e-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="c0b6e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="c0b6e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0b6e-112">Parameters</span></span>

 <span data-ttu-id="c0b6e-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="c0b6e-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="c0b6e-114">[out] Указатель на место, к которому эта функция записывает структуру [SPropValue](spropvalue.md) определение значение скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="c0b6e-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="c0b6e-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="c0b6e-116">[in] Указатель на структуру [SPropValue](spropvalue.md) , которое содержит значение свойства для копирования.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="c0b6e-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="c0b6e-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="c0b6e-118">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , можно использовать для выделения дополнительной памяти, если в месте назначения недостаточно для хранения свойства для копирования.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="c0b6e-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="c0b6e-119">_lpvObject_</span></span>
  
> <span data-ttu-id="c0b6e-120">[in] Указатель на объект, для которого **MAPIAllocateMore** будет выделить пространство, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0b6e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="c0b6e-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c0b6e-122">S_OK</span></span>
  
> <span data-ttu-id="c0b6e-123">Копирование значения одного свойства было выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="c0b6e-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c0b6e-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="c0b6e-125">Обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0b6e-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0b6e-126">Remarks</span></span>

<span data-ttu-id="c0b6e-127">Клиентское приложение или поставщик услуг можно использовать функцию **PropCopyMore** для копирования свойство из таблицы, который должен освободить для использования в других местах.</span><span class="sxs-lookup"><span data-stu-id="c0b6e-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="c0b6e-128">**PropCopyMore** не нужно выделить память, пока скопированы значение свойства типа, например PT_STRING8, который не помещается в структуре [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b6e-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="c0b6e-129">Для этих свойств больших функцию выделение памяти, с помощью функции [MAPIAllocateMore](mapiallocatemore.md) , к которому передается указатель в параметре _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="c0b6e-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="c0b6e-130">Injudicious использования памяти фрагментов **PropCopyMore** ; Рекомендуется использовать функцию [ScCopyProps](sccopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b6e-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

