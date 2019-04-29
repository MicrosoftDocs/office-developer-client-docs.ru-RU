---
title: Имсгсторенотифиневмаил
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a8ec06fd0401a129e08a06acdb1c18785f90d4a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431780"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="86c87-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="86c87-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="86c87-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86c87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86c87-105">����������� ��������� ���������, ����� ���������.</span><span class="sxs-lookup"><span data-stu-id="86c87-105">Informs the message store that a new message has arrived.</span></span> <span data-ttu-id="86c87-106">���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="86c87-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="86c87-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="86c87-107">Parameters</span></span>

 <span data-ttu-id="86c87-108">_Лпнотификатион_</span><span class="sxs-lookup"><span data-stu-id="86c87-108">_lpNotification_</span></span>
  
> <span data-ttu-id="86c87-109">[in] ��������� �� ��������� [�����������](notification.md) � ��������� ����������� � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="86c87-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="86c87-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86c87-110">Return value</span></span>

<span data-ttu-id="86c87-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="86c87-111">S_OK</span></span> 
  
> <span data-ttu-id="86c87-112">��������� ��������� ������� �����������.</span><span class="sxs-lookup"><span data-stu-id="86c87-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86c87-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="86c87-113">Remarks</span></span>

<span data-ttu-id="86c87-114">����� **IMsgStore::NotifyNewMail** ���������� ����������� ������� MAPI ��� ���������� ��������� ���������, ��� ��������� ������ ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="86c87-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="86c87-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="86c87-115">Notes to implementers</span></span>

<span data-ttu-id="86c87-p102">��� ������ **NotifyNewMail** ��������� ����������� � ��������� ����� ���� ������������������ �������������. ����� ��������� �����������, ������ [IMAPISupport::Notify](imapisupport-notify.md), ���� �� ������ ������������ ������ ������� ��������� ��� � ������� ����������� ����������. ������������������ �������� � ��� ���� � ������ [IMsgStore::Advise](imsgstore-advise.md) , ���������� ��� ���������  _lpEntryID_ �������� NULL, ��������  _ulEventMask_ ���  _fnevNewMail_.</span><span class="sxs-lookup"><span data-stu-id="86c87-p102">When **NotifyNewMail** is called, send a new mail notification to all registered clients. You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation. A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="86c87-p103">�� ��������� � �� ���������� ������ ��� ��������� [�����������](notification.md) � ��������� ����������� � ��������� �����. ���������� ��������� **NOTIFICATION**, ������ ��������������� ������� [ScCopyNotifications](sccopynotifications.md) , ����� ������������ �������� � ��� ������.</span><span class="sxs-lookup"><span data-stu-id="86c87-p103">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification. Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86c87-121">См. также</span><span class="sxs-lookup"><span data-stu-id="86c87-121">See also</span></span>



[<span data-ttu-id="86c87-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="86c87-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="86c87-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="86c87-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="86c87-124">�����������</span><span class="sxs-lookup"><span data-stu-id="86c87-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="86c87-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="86c87-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="86c87-126">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="86c87-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

