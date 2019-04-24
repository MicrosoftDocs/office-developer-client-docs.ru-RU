---
title: Иперсистмессажеисдирти
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309613"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="4fa10-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="4fa10-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="4fa10-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fa10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fa10-105">Проверяет форму на наличие изменений, выполненных с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="4fa10-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="4fa10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fa10-106">Parameters</span></span>

<span data-ttu-id="4fa10-107">Нет</span><span class="sxs-lookup"><span data-stu-id="4fa10-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="4fa10-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fa10-108">Return value</span></span>

<span data-ttu-id="4fa10-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fa10-109">S_OK</span></span> 
  
> <span data-ttu-id="4fa10-110">Форма содержит изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="4fa10-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="4fa10-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="4fa10-111">S_FALSE</span></span> 
  
> <span data-ttu-id="4fa10-112">В форме не внесены изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="4fa10-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fa10-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="4fa10-113">Remarks</span></span>

<span data-ttu-id="4fa10-114">Средства просмотра форм вызывают метод **иперсистмессаже:: IsDirty** , чтобы определить, содержит ли сообщение несохраненные данные.</span><span class="sxs-lookup"><span data-stu-id="4fa10-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fa10-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4fa10-115">See also</span></span>



[<span data-ttu-id="4fa10-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fa10-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

