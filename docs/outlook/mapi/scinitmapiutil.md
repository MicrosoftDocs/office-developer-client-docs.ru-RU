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
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420593"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="b3f88-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="b3f88-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="b3f88-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3f88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3f88-105">Заменяет [MAPIInitialize,](mapiinitialize.md) если используются только выбранные функции.</span><span class="sxs-lookup"><span data-stu-id="b3f88-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3f88-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b3f88-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3f88-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b3f88-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b3f88-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b3f88-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3f88-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3f88-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3f88-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b3f88-110">Called by:</span></span>  <br/> |<span data-ttu-id="b3f88-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="b3f88-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b3f88-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3f88-112">Parameters</span></span>

 <span data-ttu-id="b3f88-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3f88-113">_ulFlags_</span></span>
  
> <span data-ttu-id="b3f88-114">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="b3f88-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b3f88-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3f88-115">Return value</span></span>

<span data-ttu-id="b3f88-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3f88-116">S_OK</span></span> 
  
> <span data-ttu-id="b3f88-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b3f88-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3f88-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3f88-118">Remarks</span></span>

<span data-ttu-id="b3f88-119">Функции **ScInitMapiUtil** и [DeinitMapiUtil](deinitmapiutil.md) взаимодействуют для вызова и выпуска функций выбора, в отличие от [MAPIInitialize,](mapiinitialize.md)который вызывает основные, а также сканальные функции.</span><span class="sxs-lookup"><span data-stu-id="b3f88-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="b3f88-120">Когда **ScInitMapiUtil** вызывает функции с программами, он также инициализирует необходимую память.</span><span class="sxs-lookup"><span data-stu-id="b3f88-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="b3f88-121">После завершения использования функций, которые **scInitMapiUtil** вызвал, необходимо явно **вызвано DeinitMapiUtil,** чтобы освободить их.</span><span class="sxs-lookup"><span data-stu-id="b3f88-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="b3f88-122">С другой **стороны, MAPIInitialize** неявно вызывает **DeinitMapiUtil.**</span><span class="sxs-lookup"><span data-stu-id="b3f88-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3f88-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b3f88-123">See also</span></span>



[<span data-ttu-id="b3f88-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="b3f88-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

