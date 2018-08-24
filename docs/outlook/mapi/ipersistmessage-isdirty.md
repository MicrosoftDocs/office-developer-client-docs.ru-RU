---
title: IPersistMessageIsDirty
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
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576206"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="437b1-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="437b1-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="437b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="437b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="437b1-105">Проверяет формы для изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="437b1-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="437b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="437b1-106">Parameters</span></span>

<span data-ttu-id="437b1-107">None</span><span class="sxs-lookup"><span data-stu-id="437b1-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="437b1-108">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="437b1-108">Return value</span></span>

<span data-ttu-id="437b1-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="437b1-109">S_OK</span></span> 
  
> <span data-ttu-id="437b1-110">Форма содержит изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="437b1-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="437b1-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="437b1-111">S_FALSE</span></span> 
  
> <span data-ttu-id="437b1-112">Форма не имеет изменения, внесенные с момента последнего сохранения.</span><span class="sxs-lookup"><span data-stu-id="437b1-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="437b1-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="437b1-113">Remarks</span></span>

<span data-ttu-id="437b1-114">Средства просмотра формы вызовите метод **IPersistMessage::IsDirty** , чтобы определить, имеет ли сообщение несохраненные данные.</span><span class="sxs-lookup"><span data-stu-id="437b1-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="437b1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="437b1-115">See also</span></span>



[<span data-ttu-id="437b1-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="437b1-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

