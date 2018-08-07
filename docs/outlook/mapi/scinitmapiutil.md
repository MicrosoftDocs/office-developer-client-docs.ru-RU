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
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812201"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="819a7-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="819a7-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="819a7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="819a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="819a7-105">Заменяет [MAPIInitialize](mapiinitialize.md) при использовании только функции select служебной программы.</span><span class="sxs-lookup"><span data-stu-id="819a7-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="819a7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="819a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="819a7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="819a7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="819a7-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="819a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="819a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="819a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="819a7-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="819a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="819a7-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="819a7-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="819a7-112">���������</span><span class="sxs-lookup"><span data-stu-id="819a7-112">Parameters</span></span>

 <span data-ttu-id="819a7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="819a7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="819a7-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="819a7-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="819a7-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="819a7-115">Return value</span></span>

<span data-ttu-id="819a7-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="819a7-116">S_OK</span></span> 
  
> <span data-ttu-id="819a7-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="819a7-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="819a7-118">���������</span><span class="sxs-lookup"><span data-stu-id="819a7-118">Remarks</span></span>

<span data-ttu-id="819a7-119">Функции **ScInitMapiUtil** и [DeinitMapiUtil](deinitmapiutil.md) сотрудничать для вызова и освобождать функции функции, в отличие от [MAPIInitialize](mapiinitialize.md), который вызывает основной, а также служебной программы выберите программы.</span><span class="sxs-lookup"><span data-stu-id="819a7-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="819a7-120">Когда **ScInitMapiUtil** вызывает функции служебной программы, он также инициализирует необходимые памяти.</span><span class="sxs-lookup"><span data-stu-id="819a7-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="819a7-121">По завершении использования функций, которые вызвали **ScInitMapiUtil** **DeinitMapiUtil** необходимо явно вызывать для освобождения их.</span><span class="sxs-lookup"><span data-stu-id="819a7-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="819a7-122">С другой стороны **MAPIInitialize** неявно вызывает **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="819a7-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="819a7-123">См. также</span><span class="sxs-lookup"><span data-stu-id="819a7-123">See also</span></span>



[<span data-ttu-id="819a7-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="819a7-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

