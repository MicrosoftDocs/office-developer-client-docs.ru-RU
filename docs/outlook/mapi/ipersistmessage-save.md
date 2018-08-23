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
ms.openlocfilehash: 1a95989cea7ad5529eb73276b4c771e4900804b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579902"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="b4316-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="b4316-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="b4316-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4316-105">Сохраняет измененную форму сообщение, из которого его загрузки или создан.</span><span class="sxs-lookup"><span data-stu-id="b4316-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="b4316-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4316-106">Parameters</span></span>

 <span data-ttu-id="b4316-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="b4316-107">_pMessage_</span></span>
  
> <span data-ttu-id="b4316-108">[in] Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="b4316-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="b4316-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="b4316-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="b4316-110">[in] TRUE, чтобы указать, что сообщение, на который указывает, _pMessage_ сообщение, из которого форма загрузки или создания; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="b4316-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4316-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b4316-111">Return value</span></span>

<span data-ttu-id="b4316-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b4316-112">S_OK</span></span> 
  
> <span data-ttu-id="b4316-113">Форма успешно сохранен.</span><span class="sxs-lookup"><span data-stu-id="b4316-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4316-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4316-114">Remarks</span></span>

<span data-ttu-id="b4316-115">Средства просмотра форм вызовите метод **IPersistMessage::Save** для сохранения оптимизированная формы в сообщении, из которого его загрузки или создан.</span><span class="sxs-lookup"><span data-stu-id="b4316-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="b4316-116">**Сохраните** вызывается только когда форма находится в состоянии [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="b4316-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b4316-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b4316-117">Notes to implementers</span></span>

<span data-ttu-id="b4316-118">Не применить сохраненные изменения; Это вызывающий объект должен сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="b4316-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="b4316-119">Никогда не вносить изменения свойств, относящихся к сообщению формы, за исключением во время вызова **Сохранить** .</span><span class="sxs-lookup"><span data-stu-id="b4316-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="b4316-120">Если _fSameAsLoad_ имеет значение TRUE, можно сохранить изменения в существующее сообщение формы.</span><span class="sxs-lookup"><span data-stu-id="b4316-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="b4316-121">Если _fSameAsLoad_ имеет значение FALSE, необходимо скопировать все свойства из исходного сообщения в сообщения, на который указывает _pMessage_ перед выполнением сохранения.</span><span class="sxs-lookup"><span data-stu-id="b4316-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="b4316-122">Метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения служит для копирования свойств.</span><span class="sxs-lookup"><span data-stu-id="b4316-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="b4316-123">При копировании все свойства введите состояние [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="b4316-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="b4316-124">При отсутствии ошибок возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b4316-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="b4316-125">В противном случае возвращает ошибку из неудачных действия.</span><span class="sxs-lookup"><span data-stu-id="b4316-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="b4316-126">Если **Сохранить** вызывается, когда форма находится в любом состоянии, кроме Normal, возвратите значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b4316-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="b4316-127">Дополнительные сведения о сохранении объектов хранилища документации для методов [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b4316-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4316-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b4316-128">See also</span></span>



[<span data-ttu-id="b4316-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4316-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="b4316-130">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="b4316-130">Form States</span></span>](form-states.md)

