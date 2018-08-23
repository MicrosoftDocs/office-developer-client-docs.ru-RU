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
ms.openlocfilehash: 5803441486f01883d08cd99048d8eae133cd3f14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592131"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="26d58-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="26d58-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="26d58-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26d58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26d58-105">Обновление состояния в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="26d58-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="26d58-106">Поставщик хранения периодически вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="26d58-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="26d58-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="26d58-107">Parameters</span></span>

 <span data-ttu-id="26d58-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="26d58-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="26d58-109">Указатель на строку, которая отображает текущий этап хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="26d58-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="26d58-110">Она может быть NULL для отслеживания хода выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="26d58-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="26d58-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="26d58-111">**ulIndex**</span></span>
  
> <span data-ttu-id="26d58-112">Текущую позицию в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="26d58-112">The current position in progress.</span></span>
    
 <span data-ttu-id="26d58-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="26d58-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="26d58-114">Индекс, указывающее полный хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="26d58-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26d58-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="26d58-115">Return value</span></span>

<span data-ttu-id="26d58-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="26d58-116">S_OK</span></span> 
  
> <span data-ttu-id="26d58-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="26d58-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26d58-118">См. также</span><span class="sxs-lookup"><span data-stu-id="26d58-118">See also</span></span>



[<span data-ttu-id="26d58-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26d58-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

