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
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404472"
---
# <a name="propcopymore"></a><span data-ttu-id="c4bcb-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="c4bcb-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="c4bcb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4bcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4bcb-105">Копирует одно значение свойства из расположения источника в пункт назначения.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4bcb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c4bcb-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4bcb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c4bcb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c4bcb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c4bcb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4bcb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4bcb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4bcb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c4bcb-110">Called by:</span></span>  <br/> |<span data-ttu-id="c4bcb-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c4bcb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="c4bcb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="c4bcb-112">Parameters</span></span>

 <span data-ttu-id="c4bcb-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="c4bcb-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="c4bcb-114">[вышел] Указатель на расположение, в которое эта функция записывает [структуру SPropValue,](spropvalue.md) определяя значение скопированных свойств.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="c4bcb-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="c4bcb-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="c4bcb-116">[in] Указатель на [структуру SPropValue,](spropvalue.md) которая содержит скопированное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="c4bcb-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="c4bcb-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="c4bcb-118">[in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти, если расположение назначения недостаточно велико, чтобы скопировать свойство.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="c4bcb-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="c4bcb-119">_lpvObject_</span></span>
  
> <span data-ttu-id="c4bcb-120">[in] Указатель на объект, для которого **MAPIAllocateMore** будет выделять пространство при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c4bcb-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4bcb-121">Return value</span></span>

<span data-ttu-id="c4bcb-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4bcb-122">S_OK</span></span>
  
> <span data-ttu-id="c4bcb-123">Одно свойство было успешно скопировано.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="c4bcb-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c4bcb-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="c4bcb-125">Неизвестен тип свойства.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4bcb-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4bcb-126">Remarks</span></span>

<span data-ttu-id="c4bcb-127">Клиентские приложения или поставщик услуг могут использовать функцию **PropCopyMore** для копирования свойства из таблицы, которая будет освобождена, чтобы использовать его в другом месте.</span><span class="sxs-lookup"><span data-stu-id="c4bcb-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="c4bcb-128">**PropCopyMore** не нужно выделять память, если скопированное значение свойства не имеет типа, например PT_STRING8, который не вписывается в структуру [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="c4bcb-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="c4bcb-129">Для этих больших свойств функция выделяет память с помощью функции [MAPIAllocateMore,](mapiallocatemore.md) на которую передается указатель в _параметре lpfAllocMore._</span><span class="sxs-lookup"><span data-stu-id="c4bcb-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="c4bcb-130">Неоправдное использование **памяти фрагментов PropCopyMore;** вместо этого следует использовать [функцию ScCopyProps.](sccopyprops.md)</span><span class="sxs-lookup"><span data-stu-id="c4bcb-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

