---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809245"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="c70e5-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c70e5-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="c70e5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c70e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c70e5-105">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMAPITable::Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="c70e5-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c70e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c70e5-106">Parameters</span></span>

 <span data-ttu-id="c70e5-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="c70e5-107">_ulConnection_</span></span>
  
> <span data-ttu-id="c70e5-108">[in] Число подключений к регистрации, возвращаемых вызовом [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="c70e5-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c70e5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="c70e5-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c70e5-110">S_OK</span></span> 
  
> <span data-ttu-id="c70e5-111">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="c70e5-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c70e5-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="c70e5-112">Remarks</span></span>

<span data-ttu-id="c70e5-113">Используйте метод **IMAPITable::Unadvise** для освобождения указатель на объект приемника уведомлений, переданной в параметре _lpAdviseSink_ в предыдущем вызове **IMAPITable::Advise**, тем самым Отмена регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c70e5-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="c70e5-114">Как часть пропуск указатель на объект приемника уведомлений вызывается метод **функции IUnknown::Release** объекта.</span><span class="sxs-lookup"><span data-stu-id="c70e5-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="c70e5-115">Как правило, называется **выпуска** во время вызова **Unadvise** , но если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для приемник уведомлений вызова **выпуске** откладывается до **OnNotify** метод возвращает.</span><span class="sxs-lookup"><span data-stu-id="c70e5-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="c70e5-116">Дополнительные сведения о процессе уведомления видеть [Уведомления о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c70e5-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="c70e5-117">Сведения о таблице уведомлений содержатся [Уведомления о таблице](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c70e5-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="c70e5-118">Сведения об использовании методов **IMAPISupport** для поддержки уведомлений [Поддерживающие уведомления о событии](supporting-event-notification.md)см.</span><span class="sxs-lookup"><span data-stu-id="c70e5-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c70e5-119">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c70e5-119">MFCMAPI reference</span></span>

<span data-ttu-id="c70e5-120">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c70e5-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c70e5-121">**����**</span><span class="sxs-lookup"><span data-stu-id="c70e5-121">**File**</span></span>|<span data-ttu-id="c70e5-122">**�������**</span><span class="sxs-lookup"><span data-stu-id="c70e5-122">**Function**</span></span>|<span data-ttu-id="c70e5-123">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c70e5-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c70e5-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c70e5-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c70e5-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="c70e5-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="c70e5-126">Mfcmapi (en) использует метод **IMAPITable::Unadvise** для отмены уведомления для таблицы.</span><span class="sxs-lookup"><span data-stu-id="c70e5-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c70e5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c70e5-127">See also</span></span>



[<span data-ttu-id="c70e5-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c70e5-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c70e5-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="c70e5-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="c70e5-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c70e5-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c70e5-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c70e5-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

