---
title: IMsgStoreNotifyNewMail
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
ms.openlocfilehash: bdda950cd1fab66db46590e0b9141bb3d2a75221
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809378"
---
# <a name="imsgstorenotifynewmail"></a><span data-ttu-id="1f05c-103">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="1f05c-103">IMsgStore::NotifyNewMail</span></span>

  
  
<span data-ttu-id="1f05c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f05c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f05c-p101">����������� ��������� ���������, ����� ���������. ���� ����� ���������� ������ ����������� ������� MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f05c-p101">Informs the message store that a new message has arrived. This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a><span data-ttu-id="1f05c-107">���������</span><span class="sxs-lookup"><span data-stu-id="1f05c-107">Parameters</span></span>

 <span data-ttu-id="1f05c-108">_lpNotification_</span><span class="sxs-lookup"><span data-stu-id="1f05c-108">_lpNotification_</span></span>
  
> <span data-ttu-id="1f05c-109">[in] ��������� �� ��������� [�����������](notification.md) � ��������� ����������� � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="1f05c-109">[in] A pointer to a [NOTIFICATION](notification.md) structure that describes the new message notification.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f05c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="1f05c-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1f05c-111">S_OK</span></span> 
  
> <span data-ttu-id="1f05c-112">��������� ��������� ������� �����������.</span><span class="sxs-lookup"><span data-stu-id="1f05c-112">The message store was successfully notified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f05c-113">���������</span><span class="sxs-lookup"><span data-stu-id="1f05c-113">Remarks</span></span>

<span data-ttu-id="1f05c-114">����� **IMsgStore::NotifyNewMail** ���������� ����������� ������� MAPI ��� ���������� ��������� ���������, ��� ��������� ������ ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="1f05c-114">The **IMsgStore::NotifyNewMail** method is called by the MAPI spooler to inform the message store that a message is ready for delivery.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1f05c-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1f05c-115">Notes to implementers</span></span>

<span data-ttu-id="1f05c-p102">��� ������ **NotifyNewMail** ��������� ����������� � ��������� ����� ���� ������������������ �������������. ����� ��������� �����������, ������ [IMAPISupport::Notify](imapisupport-notify.md), ���� �� ������ ������������ ������ ������� ��������� ��� � ������� ����������� ����������. ������������������ �������� � ��� ���� � ������ [IMsgStore::Advise](imsgstore-advise.md) , ���������� ��� ���������  _lpEntryID_ �������� NULL, ��������  _ulEventMask_ ���  _fnevNewMail_.</span><span class="sxs-lookup"><span data-stu-id="1f05c-p102">When **NotifyNewMail** is called, send a new mail notification to all registered clients. You can send the notification by calling [IMAPISupport::Notify](imapisupport-notify.md), if you elect to use the support object methods, or by using your own implementation. A registered client is one that has called [IMsgStore::Advise](imsgstore-advise.md) and set the  _lpEntryID_ parameter to NULL and the  _ulEventMask_ parameter to  _fnevNewMail_.</span></span> 
  
<span data-ttu-id="1f05c-p103">�� ��������� � �� ���������� ������ ��� ��������� [�����������](notification.md) � ��������� ����������� � ��������� �����. ���������� ��������� **NOTIFICATION**, ������ ��������������� ������� [ScCopyNotifications](sccopynotifications.md) , ����� ������������ �������� � ��� ������.</span><span class="sxs-lookup"><span data-stu-id="1f05c-p103">Do not modify or free the memory for the [NOTIFICATION](notification.md) structure that describes the new mail notification. Copy the **NOTIFICATION** structure by calling the utility function [ScCopyNotifications](sccopynotifications.md) to make use of the information in its members.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f05c-121">��. �����</span><span class="sxs-lookup"><span data-stu-id="1f05c-121">See also</span></span>



[<span data-ttu-id="1f05c-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="1f05c-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="1f05c-123">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1f05c-123">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
  
[<span data-ttu-id="1f05c-124">�����������</span><span class="sxs-lookup"><span data-stu-id="1f05c-124">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="1f05c-125">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="1f05c-125">ScCopyNotifications</span></span>](sccopynotifications.md)
  
[<span data-ttu-id="1f05c-126">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1f05c-126">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

