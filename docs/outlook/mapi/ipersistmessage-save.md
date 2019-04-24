---
title: Иперсистмессажесаве
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
# <a name="ipersistmessagesave"></a><span data-ttu-id="f3898-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="f3898-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="f3898-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3898-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3898-105">Сохраняет измененную форму обратно в сообщение, из которого она была загружена или создана.</span><span class="sxs-lookup"><span data-stu-id="f3898-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="f3898-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3898-106">Parameters</span></span>

 <span data-ttu-id="f3898-107">_Пмессаже_</span><span class="sxs-lookup"><span data-stu-id="f3898-107">_pMessage_</span></span>
  
> <span data-ttu-id="f3898-108">возврата Указатель на сообщение.</span><span class="sxs-lookup"><span data-stu-id="f3898-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="f3898-109">_Фсамеаслоад_</span><span class="sxs-lookup"><span data-stu-id="f3898-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="f3898-110">возврата ЗНАЧЕНИЕ TRUE, чтобы указать, что сообщение, на которое указывает _пмессаже_ , является сообщением, из которого была загружена или создана форма; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="f3898-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3898-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3898-111">Return value</span></span>

<span data-ttu-id="f3898-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3898-112">S_OK</span></span> 
  
> <span data-ttu-id="f3898-113">Форма успешно сохранена.</span><span class="sxs-lookup"><span data-stu-id="f3898-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3898-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3898-114">Remarks</span></span>

<span data-ttu-id="f3898-115">Средства просмотра форм вызывают метод **иперсистмессаже:: Save** , чтобы сохранить измененную форму обратно в сообщение, из которого она была загружена или создана.</span><span class="sxs-lookup"><span data-stu-id="f3898-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="f3898-116">Метод **Save** следует вызывать только в том случае, если форма находится в [нормальном](normal-state.md) состоянии.</span><span class="sxs-lookup"><span data-stu-id="f3898-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f3898-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f3898-117">Notes to implementers</span></span>

<span data-ttu-id="f3898-118">Не зафиксируйте сохраненные изменения; Вы можете зафиксировать изменения, вызываемый абонентом.</span><span class="sxs-lookup"><span data-stu-id="f3898-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="f3898-119">Никогда не вносите изменения в свойства, принадлежащие сообщению формы, за исключением во время вызова метода **Save** .</span><span class="sxs-lookup"><span data-stu-id="f3898-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="f3898-120">Если для _фсамеаслоад_ ЗАДАНО значение true, вы можете сохранить изменения в существующем сообщении формы.</span><span class="sxs-lookup"><span data-stu-id="f3898-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="f3898-121">Если для _фсамеаслоад_ ЗАДАНО значение false, необходимо скопировать все свойства из исходного сообщения в сообщение, на которое указывает _пмессаже_ , перед выполнением сохранения.</span><span class="sxs-lookup"><span data-stu-id="f3898-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="f3898-122">Используйте метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать свойства.</span><span class="sxs-lookup"><span data-stu-id="f3898-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="f3898-123">Когда все свойства будут скопированы, введите состояние " [каракули](noscribble-state.md) ".</span><span class="sxs-lookup"><span data-stu-id="f3898-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="f3898-124">Если ошибок не возникло, возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3898-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="f3898-125">В противном случае возвращается сообщение об ошибке из действия Failed.</span><span class="sxs-lookup"><span data-stu-id="f3898-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="f3898-126">Если метод **Save** вызывается, когда форма находится в любом состоянии, кроме Normal, возвращается е_унекспектед.</span><span class="sxs-lookup"><span data-stu-id="f3898-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="f3898-127">Для получения дополнительных сведений о сохранении объектов хранилища обратитесь к документации по методу [иперсистстораже](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f3898-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3898-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f3898-128">See also</span></span>



[<span data-ttu-id="f3898-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3898-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="f3898-130">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="f3898-130">Form States</span></span>](form-states.md)

