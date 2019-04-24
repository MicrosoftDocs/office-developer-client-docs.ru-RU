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
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347770"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="44f63-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="44f63-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="44f63-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f63-105">Задает или изменяет значение одного свойства для интерфейса свойства, то есть интерфейс, производный от [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="44f63-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44f63-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="44f63-106">Header file:</span></span>  <br/> |<span data-ttu-id="44f63-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="44f63-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="44f63-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="44f63-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="44f63-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="44f63-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="44f63-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="44f63-110">Called by:</span></span>  <br/> |<span data-ttu-id="44f63-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="44f63-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="44f63-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="44f63-112">Parameters</span></span>

 <span data-ttu-id="44f63-113">_ПМП_</span><span class="sxs-lookup"><span data-stu-id="44f63-113">_pmp_</span></span>
  
> <span data-ttu-id="44f63-114">возврата Указатель на интерфейс [IMAPIProp](imapipropiunknown.md) , для которого необходимо задать или изменить значение свойства.</span><span class="sxs-lookup"><span data-stu-id="44f63-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="44f63-115">_ппроп_</span><span class="sxs-lookup"><span data-stu-id="44f63-115">_pprop_</span></span>
  
> <span data-ttu-id="44f63-116">возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую значение, которое должно быть задано для свойства _ПМП_ .</span><span class="sxs-lookup"><span data-stu-id="44f63-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44f63-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44f63-117">Return value</span></span>

<span data-ttu-id="44f63-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="44f63-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44f63-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="44f63-119">Remarks</span></span>

<span data-ttu-id="44f63-120">В отличие от метода [IMAPIProp:: SetProps](imapiprop-setprops.md) , функция **хрсетонепроп** никогда не возвращает предупреждения.</span><span class="sxs-lookup"><span data-stu-id="44f63-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="44f63-121">Так как задается только одно свойство, оно просто может быть успешным или неудачным.</span><span class="sxs-lookup"><span data-stu-id="44f63-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="44f63-122">Для настройки или изменения нескольких свойств **SetProps** быстрее.</span><span class="sxs-lookup"><span data-stu-id="44f63-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="44f63-123">Вы можете получить одно свойство с помощью функции [хржетонепроп](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="44f63-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

