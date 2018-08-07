---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809182"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="c4d7c-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="c4d7c-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="c4d7c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4d7c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4d7c-105">Обновление состояния в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="c4d7c-106">Поставщик хранения периодически вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="c4d7c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4d7c-107">Parameters</span></span>

 <span data-ttu-id="c4d7c-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="c4d7c-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="c4d7c-109">Указатель на строку, которая отображает текущий этап хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="c4d7c-110">Она может быть NULL для отслеживания хода выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="c4d7c-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="c4d7c-111">**ulIndex**</span></span>
  
> <span data-ttu-id="c4d7c-112">Текущую позицию в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-112">The current position in progress.</span></span>
    
 <span data-ttu-id="c4d7c-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="c4d7c-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="c4d7c-114">Индекс, указывающее полный хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4d7c-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c4d7c-115">Return value</span></span>

<span data-ttu-id="c4d7c-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c4d7c-116">S_OK</span></span> 
  
> <span data-ttu-id="c4d7c-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c4d7c-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4d7c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c4d7c-118">See also</span></span>



[<span data-ttu-id="c4d7c-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4d7c-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

