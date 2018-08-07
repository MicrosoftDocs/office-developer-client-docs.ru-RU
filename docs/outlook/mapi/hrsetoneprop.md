---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808697"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="a2cc2-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="a2cc2-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="a2cc2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2cc2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2cc2-105">Задает или изменяет значения одного свойства для интерфейса свойство, то есть, производные от [IMAPIProp](imapipropiunknown.md)интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a2cc2-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2cc2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a2cc2-106">Header file:</span></span>  <br/> |<span data-ttu-id="a2cc2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a2cc2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a2cc2-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="a2cc2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a2cc2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a2cc2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a2cc2-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="a2cc2-110">Called by:</span></span>  <br/> |<span data-ttu-id="a2cc2-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="a2cc2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="a2cc2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2cc2-112">Parameters</span></span>

 <span data-ttu-id="a2cc2-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="a2cc2-113">_pmp_</span></span>
  
> <span data-ttu-id="a2cc2-114">[in] Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , где значение свойства — установить или изменить.</span><span class="sxs-lookup"><span data-stu-id="a2cc2-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="a2cc2-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="a2cc2-115">_pprop_</span></span>
  
> <span data-ttu-id="a2cc2-116">[in] Указатель на структуру [SPropValue](spropvalue.md) , определяющий значение должно быть задано для свойства _pmp_ .</span><span class="sxs-lookup"><span data-stu-id="a2cc2-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a2cc2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2cc2-117">Return value</span></span>

<span data-ttu-id="a2cc2-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="a2cc2-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2cc2-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="a2cc2-119">Remarks</span></span>

<span data-ttu-id="a2cc2-120">В отличие от метода [IMAPIProp::SetProps](imapiprop-setprops.md) функция **HrSetOneProp** никогда не возвращает все предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a2cc2-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="a2cc2-121">Так как только одно свойство, он просто либо успешного или неудачного завершения.</span><span class="sxs-lookup"><span data-stu-id="a2cc2-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="a2cc2-122">Для параметра или изменение значений нескольких свойств **SetProps** выполняется быстрее.</span><span class="sxs-lookup"><span data-stu-id="a2cc2-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="a2cc2-123">Вы можете получить отдельное свойство с помощью функции [HrGetOneProp](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="a2cc2-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

