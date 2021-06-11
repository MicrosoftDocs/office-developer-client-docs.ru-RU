---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309620"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="3762e-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="3762e-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="3762e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3762e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3762e-105">Сохраняет измененную форму обратно в сообщение, из которого она была загружена или создана.</span><span class="sxs-lookup"><span data-stu-id="3762e-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="3762e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3762e-106">Parameters</span></span>

 <span data-ttu-id="3762e-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="3762e-107">_pMessage_</span></span>
  
> <span data-ttu-id="3762e-108">[in] Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="3762e-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="3762e-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="3762e-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="3762e-110">[in] TRUE указывает, что сообщение, на которое указывает  _pMessage,_ — это сообщение, из которого была загружена или создана форма; в противном случае FALSE.</span><span class="sxs-lookup"><span data-stu-id="3762e-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3762e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3762e-111">Return value</span></span>

<span data-ttu-id="3762e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3762e-112">S_OK</span></span> 
  
> <span data-ttu-id="3762e-113">Форма успешно сохранена.</span><span class="sxs-lookup"><span data-stu-id="3762e-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3762e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3762e-114">Remarks</span></span>

<span data-ttu-id="3762e-115">Зрители форм называют **метод IPersistMessage::Save,** чтобы сохранить измененную форму обратно в сообщение, из которого оно было загружено или создано.</span><span class="sxs-lookup"><span data-stu-id="3762e-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="3762e-116">**Сохранение** должно быть вызвано только в том случае, если форма находится в [нормальном состоянии.](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="3762e-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3762e-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3762e-117">Notes to implementers</span></span>

<span data-ttu-id="3762e-118">Не фиксировать сохраненные изменения; зафиксировать изменения должен вызываемая.</span><span class="sxs-lookup"><span data-stu-id="3762e-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="3762e-119">Никогда не внося изменения в свойства, которые принадлежат сообщению формы, за исключением вызова **Сохранить.**</span><span class="sxs-lookup"><span data-stu-id="3762e-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="3762e-120">Если  _для fSameAsLoad_ установлено true, можно сохранить изменения в существующем сообщении формы.</span><span class="sxs-lookup"><span data-stu-id="3762e-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="3762e-121">Если _fSameAsLoad_ задают false, перед выполнением сохранения необходимо скопировать все свойства из исходного сообщения в сообщение, на которое указывает _pMessage._</span><span class="sxs-lookup"><span data-stu-id="3762e-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="3762e-122">Используйте метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения для копирования свойств.</span><span class="sxs-lookup"><span data-stu-id="3762e-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="3762e-123">После копирования всех свойств введите [состояние NoScribble.](noscribble-state.md)</span><span class="sxs-lookup"><span data-stu-id="3762e-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="3762e-124">Если ошибки не происходят, S_OK.</span><span class="sxs-lookup"><span data-stu-id="3762e-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="3762e-125">В противном случае возвращаем ошибку из неудатного действия.</span><span class="sxs-lookup"><span data-stu-id="3762e-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="3762e-126">Если **сохранить** называется, когда форма находится в любом состоянии, кроме нормального, E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="3762e-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="3762e-127">Дополнительные сведения о сохранении объектов хранения см. в документации по методам [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3762e-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3762e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3762e-128">See also</span></span>



[<span data-ttu-id="3762e-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3762e-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="3762e-130">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="3762e-130">Form States</span></span>](form-states.md)

