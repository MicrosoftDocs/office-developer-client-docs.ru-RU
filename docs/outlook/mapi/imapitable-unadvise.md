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
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430233"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="36b2b-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="36b2b-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="36b2b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36b2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36b2b-105">Отменяет отправку уведомлений, которые ранее были настроены с помощью вызова метода [IMAPITable::Advise.](imapitable-advise.md)</span><span class="sxs-lookup"><span data-stu-id="36b2b-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="36b2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36b2b-106">Parameters</span></span>

 <span data-ttu-id="36b2b-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="36b2b-107">_ulConnection_</span></span>
  
> <span data-ttu-id="36b2b-108">[in] Номер подключения регистрации, возвращенный вызовом [IMAPITable::Advise.](imapitable-advise.md)</span><span class="sxs-lookup"><span data-stu-id="36b2b-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36b2b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36b2b-109">Return value</span></span>

<span data-ttu-id="36b2b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="36b2b-110">S_OK</span></span> 
  
> <span data-ttu-id="36b2b-111">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="36b2b-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36b2b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="36b2b-112">Remarks</span></span>

<span data-ttu-id="36b2b-113">Используйте метод **IMAPITable::Unadvise,** чтобы освободить указатель на объект приемника рекомендации, переданный в  _параметре lpAdviseSink_ в предыдущем вызове **IMAPITable::Advise,** тем самым отменив регистрацию уведомления.</span><span class="sxs-lookup"><span data-stu-id="36b2b-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="36b2b-114">При удалении указателя на объект приемника рекомендации будет вызван метод **IUnknown::Release** объекта.</span><span class="sxs-lookup"><span data-stu-id="36b2b-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="36b2b-115">Как **правило,** выпуск вызывается во время вызова **Unadvise,** но если другой поток вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для приемника рекомендации, вызов release откладывается до тех пор, пока не будет возвращен метод **OnNotify.** </span><span class="sxs-lookup"><span data-stu-id="36b2b-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="36b2b-116">Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="36b2b-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="36b2b-117">Конкретные сведения об уведомлении таблицы [см. в таблице уведомлений.](about-table-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="36b2b-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="36b2b-118">Сведения об использовании методов **IMAPISupport** для поддержки уведомлений см. в подразделе ["Поддержка уведомления о событии".](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="36b2b-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36b2b-119">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36b2b-119">MFCMAPI reference</span></span>

<span data-ttu-id="36b2b-120">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="36b2b-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36b2b-121">**Файл**</span><span class="sxs-lookup"><span data-stu-id="36b2b-121">**File**</span></span>|<span data-ttu-id="36b2b-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="36b2b-122">**Function**</span></span>|<span data-ttu-id="36b2b-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="36b2b-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36b2b-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="36b2b-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="36b2b-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="36b2b-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="36b2b-126">MFCMAPI использует метод **IMAPITable::Unadvise** для отмены уведомлений для таблицы.</span><span class="sxs-lookup"><span data-stu-id="36b2b-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36b2b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="36b2b-127">See also</span></span>



[<span data-ttu-id="36b2b-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="36b2b-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="36b2b-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="36b2b-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="36b2b-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36b2b-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="36b2b-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="36b2b-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

