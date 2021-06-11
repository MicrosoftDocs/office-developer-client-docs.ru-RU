---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418724"
---
# <a name="getinstance"></a><span data-ttu-id="d8e91-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="d8e91-103">GetInstance</span></span>

  
  
<span data-ttu-id="d8e91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8e91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8e91-105">Копирует одно значение в многоценном свойстве в одноценное свойство того же типа.</span><span class="sxs-lookup"><span data-stu-id="d8e91-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8e91-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d8e91-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8e91-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="d8e91-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="d8e91-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d8e91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8e91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8e91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8e91-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d8e91-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8e91-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d8e91-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="d8e91-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8e91-112">Parameters</span></span>

 <span data-ttu-id="d8e91-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="d8e91-113">_pvalMv_</span></span>
  
> <span data-ttu-id="d8e91-114">[in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей многоценное свойство.</span><span class="sxs-lookup"><span data-stu-id="d8e91-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="d8e91-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="d8e91-115">_pvalSv_</span></span>
  
> <span data-ttu-id="d8e91-116">[in] Указатель на одно значение свойства для получения данных.</span><span class="sxs-lookup"><span data-stu-id="d8e91-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="d8e91-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="d8e91-117">_uliInst_</span></span>
  
> <span data-ttu-id="d8e91-118">[in] Номер экземпляра, то есть элемент массива, значения, копируется из структуры, обозначенной _параметром pvalMv._</span><span class="sxs-lookup"><span data-stu-id="d8e91-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8e91-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8e91-119">Return value</span></span>

<span data-ttu-id="d8e91-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="d8e91-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8e91-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="d8e91-121">Remarks</span></span>

<span data-ttu-id="d8e91-122">Если копированное значение слишком велико для выделенной памяти, функция **GetInstance** копирует только указатели, а не выделяет новую память.</span><span class="sxs-lookup"><span data-stu-id="d8e91-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

