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
# <a name="propcopymore"></a><span data-ttu-id="27ade-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="27ade-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="27ade-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27ade-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27ade-105">Копирует одно значение свойства из исходного расположения в конечное расположение.</span><span class="sxs-lookup"><span data-stu-id="27ade-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27ade-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27ade-106">Header file:</span></span>  <br/> |<span data-ttu-id="27ade-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="27ade-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="27ade-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="27ade-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27ade-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27ade-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27ade-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="27ade-110">Called by:</span></span>  <br/> |<span data-ttu-id="27ade-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="27ade-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="27ade-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="27ade-112">Parameters</span></span>

 <span data-ttu-id="27ade-113">_лпспропвалуедест_</span><span class="sxs-lookup"><span data-stu-id="27ade-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="27ade-114">вышли Указатель на расположение, в которое эта функция записывает структуру [спропвалуе](spropvalue.md) , определяющую значение скопированного свойства.</span><span class="sxs-lookup"><span data-stu-id="27ade-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="27ade-115">_лпспропвалуесрк_</span><span class="sxs-lookup"><span data-stu-id="27ade-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="27ade-116">возврата Указатель на структуру [спропвалуе](spropvalue.md) , содержащую копируемое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="27ade-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="27ade-117">_лпфаллокморе_</span><span class="sxs-lookup"><span data-stu-id="27ade-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="27ade-118">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти, если целевое расположение недостаточно велико для хранения свойства, которое необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="27ade-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="27ade-119">_лпвобжект_</span><span class="sxs-lookup"><span data-stu-id="27ade-119">_lpvObject_</span></span>
  
> <span data-ttu-id="27ade-120">возврата Указатель на объект, для которого **мапиаллокатеморе** будет выделять место при необходимости.</span><span class="sxs-lookup"><span data-stu-id="27ade-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27ade-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27ade-121">Return value</span></span>

<span data-ttu-id="27ade-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="27ade-122">S_OK</span></span>
  
> <span data-ttu-id="27ade-123">Значение одного свойства было успешно скопировано.</span><span class="sxs-lookup"><span data-stu-id="27ade-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="27ade-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="27ade-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="27ade-125">Обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="27ade-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27ade-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="27ade-126">Remarks</span></span>

<span data-ttu-id="27ade-127">Клиентское приложение или поставщик услуг может использовать функцию **пропкопиморе** , чтобы скопировать свойство из таблицы, которая будет освобождена, чтобы использовать ее в других целях.</span><span class="sxs-lookup"><span data-stu-id="27ade-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="27ade-128">**Пропкопиморе** не требует выделения памяти, если не копируется значение свойства типа, такого как PT_STRING8, которое не помещается в структуру [спропвалуе](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="27ade-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="27ade-129">Для этих больших свойств функция выделяет память с помощью функции [мапиаллокатеморе](mapiallocatemore.md) , в которую передается указатель в параметре _лпфаллокморе_ .</span><span class="sxs-lookup"><span data-stu-id="27ade-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="27ade-130">Неразумное использование памяти для фрагментов **пропкопиморе** ; Вместо этого рекомендуется использовать функцию [сккопипропс](sccopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="27ade-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

