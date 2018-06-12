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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808550"
---
# <a name="getinstance"></a><span data-ttu-id="818a9-103">GetInstance</span><span class="sxs-lookup"><span data-stu-id="818a9-103">GetInstance</span></span>

  
  
<span data-ttu-id="818a9-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="818a9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="818a9-105">Копирует одно значение в рамках свойством одним значением свойства одного типа.</span><span class="sxs-lookup"><span data-stu-id="818a9-105">Copies one value within a multivalued property to a single-valued property of the same type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="818a9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="818a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="818a9-107">MAPIUTIL. H</span><span class="sxs-lookup"><span data-stu-id="818a9-107">MAPIUTIL.H</span></span>  <br/> |
|<span data-ttu-id="818a9-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="818a9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="818a9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="818a9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="818a9-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="818a9-110">Called by:</span></span>  <br/> |<span data-ttu-id="818a9-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="818a9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a><span data-ttu-id="818a9-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="818a9-112">Parameters</span></span>

 <span data-ttu-id="818a9-113">_pvalMv_</span><span class="sxs-lookup"><span data-stu-id="818a9-113">_pvalMv_</span></span>
  
> <span data-ttu-id="818a9-114">[in] Указатель на структуру [SPropValue](spropvalue.md) определения многозначные свойства.</span><span class="sxs-lookup"><span data-stu-id="818a9-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining a multivalued property.</span></span> 
    
 <span data-ttu-id="818a9-115">_pvalSv_</span><span class="sxs-lookup"><span data-stu-id="818a9-115">_pvalSv_</span></span>
  
> <span data-ttu-id="818a9-116">[in] Указатель на поддерживающий одно свойство для получения данных.</span><span class="sxs-lookup"><span data-stu-id="818a9-116">[in] Pointer to a single-valued property to receive data.</span></span> 
    
 <span data-ttu-id="818a9-117">_uliInst_</span><span class="sxs-lookup"><span data-stu-id="818a9-117">_uliInst_</span></span>
  
> <span data-ttu-id="818a9-118">[in] Номер экземпляра, который является, элемент массива копируются из структуры, указанное с помощью параметра _pvalMv_ значения.</span><span class="sxs-lookup"><span data-stu-id="818a9-118">[in] The instance number, that is, the array element, of the value being copied from the structure indicated by the  _pvalMv_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="818a9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="818a9-119">Return value</span></span>

<span data-ttu-id="818a9-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="818a9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="818a9-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="818a9-121">Remarks</span></span>

<span data-ttu-id="818a9-122">Если значение копируются слишком велик для выделенной памяти, функция **GetInstance** копирует только указателей вместо выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="818a9-122">If the value copied is too large for the allocated memory, the **GetInstance** function only copies pointers instead of allocating new memory.</span></span> 
  

