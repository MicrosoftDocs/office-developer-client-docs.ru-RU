---
title: Имаписинкпрогресскаллбаккпрогресс
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
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429112"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="c7d1a-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="c7d1a-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="c7d1a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7d1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7d1a-105">Обновляет состояние в диалоговом окне отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="c7d1a-106">Поставщик хранилища периодически вызывает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="c7d1a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7d1a-107">Parameters</span></span>

 <span data-ttu-id="c7d1a-108">**Пвкзспрогресс**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="c7d1a-109">Указатель на строку, отображающую текущий этап хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="c7d1a-110">Для обновления хода выполнения может быть задано значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="c7d1a-111">**Улиндекс**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-111">**ulIndex**</span></span>
  
> <span data-ttu-id="c7d1a-112">Текущая позиция в ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-112">The current position in progress.</span></span>
    
 <span data-ttu-id="c7d1a-113">**Улиндексмакс**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="c7d1a-114">Индекс, указывающий на завершение процесса.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7d1a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7d1a-115">Return value</span></span>

<span data-ttu-id="c7d1a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7d1a-116">S_OK</span></span> 
  
> <span data-ttu-id="c7d1a-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7d1a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c7d1a-118">See also</span></span>



[<span data-ttu-id="c7d1a-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7d1a-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

