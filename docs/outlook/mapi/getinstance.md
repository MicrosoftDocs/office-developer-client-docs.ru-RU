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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299547"
---
# <a name="getinstance"></a><span data-ttu-id="1d677-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="1d677-103">GetInstance</span></span>

  
  
<span data-ttu-id="1d677-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d677-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d677-105">Копирует одно значение из многозначного свойства в свойство с одним значением того же типа.</span><span class="sxs-lookup"><span data-stu-id="1d677-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d677-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1d677-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d677-107">МАПИУТИЛ. Высоты</span><span class="sxs-lookup"><span data-stu-id="1d677-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="1d677-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1d677-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1d677-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1d677-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1d677-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1d677-110">Called by:</span></span>  <br/> |<span data-ttu-id="1d677-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1d677-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="1d677-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d677-112">Parameters</span></span>

 <span data-ttu-id="1d677-113">_Пвалмв_</span><span class="sxs-lookup"><span data-stu-id="1d677-113">_pvalMv_</span></span>
  
> <span data-ttu-id="1d677-114">возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую многозначное свойство.</span><span class="sxs-lookup"><span data-stu-id="1d677-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="1d677-115">_Пвалсв_</span><span class="sxs-lookup"><span data-stu-id="1d677-115">_pvalSv_</span></span>
  
> <span data-ttu-id="1d677-116">возврата Указатель на свойство с одним значением, чтобы получить данные.</span><span class="sxs-lookup"><span data-stu-id="1d677-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="1d677-117">_Улиинст_</span><span class="sxs-lookup"><span data-stu-id="1d677-117">_uliInst_</span></span>
  
> <span data-ttu-id="1d677-118">возврата Номер экземпляра (то есть, элемент массива) значения копируется из структуры, указанной параметром _пвалмв_ .</span><span class="sxs-lookup"><span data-stu-id="1d677-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d677-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d677-119">Return value</span></span>

<span data-ttu-id="1d677-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="1d677-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d677-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d677-121">Remarks</span></span>

<span data-ttu-id="1d677-122">Если копируемое значение слишком велико для выделенной памяти, функция **GetInstance** копирует только указатели вместо выделения новой памяти.</span><span class="sxs-lookup"><span data-stu-id="1d677-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

