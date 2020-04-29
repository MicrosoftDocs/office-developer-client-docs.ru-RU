---
title: иперсистмессажеисдирти
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407573"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="082a0-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="082a0-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="082a0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="082a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="082a0-105">Проверяет форму на наличие изменений, выполненных с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="082a0-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="082a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="082a0-106">Parameters</span></span>

<span data-ttu-id="082a0-107">Нет</span><span class="sxs-lookup"><span data-stu-id="082a0-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="082a0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="082a0-108">Return value</span></span>

<span data-ttu-id="082a0-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="082a0-109">S_OK</span></span> 
  
> <span data-ttu-id="082a0-110">Форма содержит изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="082a0-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="082a0-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="082a0-111">S_FALSE</span></span> 
  
> <span data-ttu-id="082a0-112">В форме не внесены изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="082a0-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="082a0-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="082a0-113">Remarks</span></span>

<span data-ttu-id="082a0-114">Средства просмотра форм вызывают метод **иперсистмессаже:: IsDirty** , чтобы определить, содержит ли сообщение несохраненные данные.</span><span class="sxs-lookup"><span data-stu-id="082a0-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="082a0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="082a0-115">See also</span></span>



[<span data-ttu-id="082a0-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="082a0-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

