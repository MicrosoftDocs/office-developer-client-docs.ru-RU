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
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589182"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="1af43-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="1af43-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="1af43-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1af43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1af43-105">Задает или изменяет значение одного свойства в интерфейсе свойств, то есть интерфейс, полученный из [IMAPIProp.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1af43-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1af43-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1af43-106">Header file:</span></span>  <br/> |<span data-ttu-id="1af43-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1af43-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1af43-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1af43-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1af43-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1af43-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1af43-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1af43-110">Called by:</span></span>  <br/> |<span data-ttu-id="1af43-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1af43-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="1af43-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1af43-112">Parameters</span></span>

 <span data-ttu-id="1af43-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="1af43-113">_pmp_</span></span>
  
> <span data-ttu-id="1af43-114">[in] Указатель на [интерфейс IMAPIProp,](imapipropiunknown.md) на котором должно быть установлено или изменено значение свойства.</span><span class="sxs-lookup"><span data-stu-id="1af43-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="1af43-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="1af43-115">_pprop_</span></span>
  
> <span data-ttu-id="1af43-116">[in] Указатель на [структуру SPropValue,](spropvalue.md) определяющий значение, запредельное для _свойства pmp._</span><span class="sxs-lookup"><span data-stu-id="1af43-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1af43-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1af43-117">Return value</span></span>

<span data-ttu-id="1af43-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="1af43-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1af43-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="1af43-119">Remarks</span></span>

<span data-ttu-id="1af43-120">В отличие [от метода IMAPIProp::SetProps,](imapiprop-setprops.md) функция **HrSetOneProp** никогда не возвращает предупреждений.</span><span class="sxs-lookup"><span data-stu-id="1af43-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="1af43-121">Так как оно задает только одно свойство, оно просто успешно или не удается.</span><span class="sxs-lookup"><span data-stu-id="1af43-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="1af43-122">Для настройки или изменения нескольких свойств **SetProps быстрее.**</span><span class="sxs-lookup"><span data-stu-id="1af43-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="1af43-123">Вы можете получить одно свойство с помощью [функции HrGetOneProp.](hrgetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="1af43-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

