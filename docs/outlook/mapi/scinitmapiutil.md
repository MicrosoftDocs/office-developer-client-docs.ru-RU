---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575037"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="331c4-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="331c4-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="331c4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="331c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="331c4-105">Заменяет [MAPIInitialize](mapiinitialize.md) при использовании только функции select служебной программы.</span><span class="sxs-lookup"><span data-stu-id="331c4-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="331c4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="331c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="331c4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="331c4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="331c4-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="331c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="331c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="331c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="331c4-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="331c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="331c4-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="331c4-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="331c4-112">���������</span><span class="sxs-lookup"><span data-stu-id="331c4-112">Parameters</span></span>

 <span data-ttu-id="331c4-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="331c4-113">_ulFlags_</span></span>
  
> <span data-ttu-id="331c4-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="331c4-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="331c4-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="331c4-115">Return value</span></span>

<span data-ttu-id="331c4-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="331c4-116">S_OK</span></span> 
  
> <span data-ttu-id="331c4-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="331c4-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="331c4-118">���������</span><span class="sxs-lookup"><span data-stu-id="331c4-118">Remarks</span></span>

<span data-ttu-id="331c4-119">Функции **ScInitMapiUtil** и [DeinitMapiUtil](deinitmapiutil.md) сотрудничать для вызова и освобождать функции функции, в отличие от [MAPIInitialize](mapiinitialize.md), который вызывает основной, а также служебной программы выберите программы.</span><span class="sxs-lookup"><span data-stu-id="331c4-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="331c4-120">Когда **ScInitMapiUtil** вызывает функции служебной программы, он также инициализирует необходимые памяти.</span><span class="sxs-lookup"><span data-stu-id="331c4-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="331c4-121">По завершении использования функций, которые вызвали **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их.</span><span class="sxs-lookup"><span data-stu-id="331c4-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="331c4-122">С другой стороны **MAPIInitialize** неявно вызывает **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="331c4-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="331c4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="331c4-123">See also</span></span>



[<span data-ttu-id="331c4-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="331c4-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

