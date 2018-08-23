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
ms.openlocfilehash: 7de4d3c58d5eeefcf9a82235333da5db4703bc8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592978"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="bf517-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="bf517-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="bf517-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf517-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf517-105">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMAPITable::Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="bf517-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bf517-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf517-106">Parameters</span></span>

 <span data-ttu-id="bf517-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="bf517-107">_ulConnection_</span></span>
  
> <span data-ttu-id="bf517-108">[in] Число подключений к регистрации, возвращаемых вызовом [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="bf517-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf517-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bf517-109">Return value</span></span>

<span data-ttu-id="bf517-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bf517-110">S_OK</span></span> 
  
> <span data-ttu-id="bf517-111">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="bf517-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf517-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf517-112">Remarks</span></span>

<span data-ttu-id="bf517-113">Используйте метод **IMAPITable::Unadvise** для освобождения указатель на объект приемника уведомлений, переданной в параметре _lpAdviseSink_ в предыдущем вызове **IMAPITable::Advise**, тем самым Отмена регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bf517-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="bf517-114">Как часть пропуск указатель на объект приемника уведомлений вызывается метод **функции IUnknown::Release** объекта.</span><span class="sxs-lookup"><span data-stu-id="bf517-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="bf517-115">Как правило, называется **выпуска** во время вызова **Unadvise** , но если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для приемник уведомлений вызова **выпуске** откладывается до **OnNotify** метод возвращает.</span><span class="sxs-lookup"><span data-stu-id="bf517-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="bf517-116">Дополнительные сведения о процессе уведомления видеть [Уведомления о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="bf517-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="bf517-117">Сведения о таблице уведомлений содержатся [Уведомления о таблице](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="bf517-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="bf517-118">Сведения об использовании методов **IMAPISupport** для поддержки уведомлений [Поддерживающие уведомления о событии](supporting-event-notification.md)см.</span><span class="sxs-lookup"><span data-stu-id="bf517-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf517-119">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="bf517-119">MFCMAPI reference</span></span>

<span data-ttu-id="bf517-120">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="bf517-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf517-121">**����**</span><span class="sxs-lookup"><span data-stu-id="bf517-121">**File**</span></span>|<span data-ttu-id="bf517-122">**�������**</span><span class="sxs-lookup"><span data-stu-id="bf517-122">**Function**</span></span>|<span data-ttu-id="bf517-123">**�����������**</span><span class="sxs-lookup"><span data-stu-id="bf517-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf517-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="bf517-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="bf517-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="bf517-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="bf517-126">Mfcmapi (en) использует метод **IMAPITable::Unadvise** для отмены уведомления для таблицы.</span><span class="sxs-lookup"><span data-stu-id="bf517-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf517-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bf517-127">See also</span></span>



[<span data-ttu-id="bf517-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bf517-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bf517-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="bf517-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="bf517-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf517-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="bf517-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bf517-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

