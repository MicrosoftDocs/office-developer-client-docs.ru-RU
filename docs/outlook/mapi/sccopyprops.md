---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351333"
---
# <a name="sccopyprops"></a><span data-ttu-id="f52d4-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="f52d4-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="f52d4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f52d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f52d4-105">Копирует свойства, определенные массивом структур [спропвалуе](spropvalue.md) , в новое назначение.</span><span class="sxs-lookup"><span data-stu-id="f52d4-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f52d4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f52d4-106">Header file:</span></span>  <br/> |<span data-ttu-id="f52d4-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="f52d4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f52d4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f52d4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f52d4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f52d4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f52d4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f52d4-110">Called by:</span></span>  <br/> |<span data-ttu-id="f52d4-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="f52d4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="f52d4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f52d4-112">Parameters</span></span>

 <span data-ttu-id="f52d4-113">_кпроп_</span><span class="sxs-lookup"><span data-stu-id="f52d4-113">_cprop_</span></span>
  
> <span data-ttu-id="f52d4-114">возврата Количество копируемых свойств.</span><span class="sxs-lookup"><span data-stu-id="f52d4-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="f52d4-115">_ргпроп_</span><span class="sxs-lookup"><span data-stu-id="f52d4-115">_rgprop_</span></span>
  
> <span data-ttu-id="f52d4-116">возврата Указатель на массив структур [спропвалуе](spropvalue.md) , определяющих копируемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f52d4-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="f52d4-117">Параметр _ргпроп_ не обязательно указывает на начало массива, но он должен указать на начало одной из структур **спропвалуе** в массиве.</span><span class="sxs-lookup"><span data-stu-id="f52d4-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="f52d4-118">_Пвдст_</span><span class="sxs-lookup"><span data-stu-id="f52d4-118">_pvDst_</span></span>
  
> <span data-ttu-id="f52d4-119">возврата Указатель на исходное положение в памяти, в которое эта функция копирует свойства.</span><span class="sxs-lookup"><span data-stu-id="f52d4-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="f52d4-120">_ПКБ_</span><span class="sxs-lookup"><span data-stu-id="f52d4-120">_pcb_</span></span>
  
> <span data-ttu-id="f52d4-121">вышли НеОбязательный указатель размера блока памяти (в байтах), на который указывает параметр _пвдст_ .</span><span class="sxs-lookup"><span data-stu-id="f52d4-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f52d4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f52d4-122">Return value</span></span>

<span data-ttu-id="f52d4-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f52d4-123">S_OK</span></span>
  
> <span data-ttu-id="f52d4-124">Свойства успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="f52d4-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="f52d4-125">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="f52d4-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="f52d4-126">Обнаружен неизвестный тип свойства.</span><span class="sxs-lookup"><span data-stu-id="f52d4-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f52d4-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="f52d4-127">Remarks</span></span>

<span data-ttu-id="f52d4-128">Новый массив и его данные находятся в буфере, созданном с одним выделением, а функция [скрелокпропс](screlocprops.md) может использоваться для изменения указателей в отдельных структурах [спропвалуе](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="f52d4-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="f52d4-129">До этой коррекции указатели являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="f52d4-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="f52d4-130">**Сккопипропс** поддерживает исходный порядок свойств для скопированного массива свойств.</span><span class="sxs-lookup"><span data-stu-id="f52d4-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="f52d4-131">Параметр _ПКБ_ является необязательным; Если он не равен NULL, то для него задается число байтов, хранящихся в параметре _пвдст_ .</span><span class="sxs-lookup"><span data-stu-id="f52d4-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f52d4-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f52d4-132">See also</span></span>



[<span data-ttu-id="f52d4-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="f52d4-133">ScDupPropset</span></span>](scduppropset.md)

