---
title: имапитаблеунадвисе
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
# <a name="imapitableunadvise"></a><span data-ttu-id="c4d4a-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="c4d4a-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="c4d4a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d4a-105">Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода [IMAPITable:: Advise](imapitable-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="c4d4a-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="c4d4a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4d4a-106">Parameters</span></span>

 <span data-ttu-id="c4d4a-107">_улконнектион_</span><span class="sxs-lookup"><span data-stu-id="c4d4a-107">_ulConnection_</span></span>
  
> <span data-ttu-id="c4d4a-108">возврата Номер подключения регистрации, возвращенный при вызове метода [IMAPITable:: Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="c4d4a-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4d4a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4d4a-109">Return value</span></span>

<span data-ttu-id="c4d4a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4d4a-110">S_OK</span></span> 
  
> <span data-ttu-id="c4d4a-111">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="c4d4a-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4d4a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4d4a-112">Remarks</span></span>

<span data-ttu-id="c4d4a-113">Используйте метод **IMAPITable::** unadvise, чтобы освободить указатель на объект приемника уведомлений, переданный в параметре _лпадвисесинк_ при предыдущем вызове метода **IMAPITable:: Advise**, тем самым отменяя регистрацию уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c4d4a-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="c4d4a-114">При отмене указателя на объект приемника уведомлений вызывается метод " **IUnknown:: Release** " объекта.</span><span class="sxs-lookup"><span data-stu-id="c4d4a-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="c4d4a-115">Как правило, **выпуск** вызывается во время вызова метода **unadvise** , но если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для приемника уведомлений, вызов **освобождения** задерживается до возвращения метода **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="c4d4a-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="c4d4a-116">Более подробную информацию о процессе уведомления можно узнать [в статье уведомление о событии в MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="c4d4a-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="c4d4a-117">Конкретные сведения о табличных [уведомлениях см.](about-table-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="c4d4a-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="c4d4a-118">Сведения о том, как использовать методы **имаписуппорт** для поддержки уведомлений, можно узнать в разделе [Поддержка уведомлений о событиях](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="c4d4a-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c4d4a-119">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c4d4a-119">MFCMAPI reference</span></span>

<span data-ttu-id="c4d4a-120">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c4d4a-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c4d4a-121">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c4d4a-121">**File**</span></span>|<span data-ttu-id="c4d4a-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c4d4a-122">**Function**</span></span>|<span data-ttu-id="c4d4a-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c4d4a-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4d4a-124">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="c4d4a-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c4d4a-125">Кконтентстаблелистктрл:: Нотификатионофф</span><span class="sxs-lookup"><span data-stu-id="c4d4a-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="c4d4a-126">MFCMAPI использует метод **IMAPITable:: unadvise** для отмены уведомлений для таблицы.</span><span class="sxs-lookup"><span data-stu-id="c4d4a-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4d4a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c4d4a-127">See also</span></span>



[<span data-ttu-id="c4d4a-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="c4d4a-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="c4d4a-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="c4d4a-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="c4d4a-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4d4a-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="c4d4a-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c4d4a-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

