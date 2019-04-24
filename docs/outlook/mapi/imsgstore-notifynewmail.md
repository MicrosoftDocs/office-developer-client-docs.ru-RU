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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348757"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
����������� ��������� ���������, ����� ���������. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Параметры

 _Лпнотификатион_
  
> [in] ��������� �� ��������� [�����������](notification.md) � ��������� ����������� � ��������� ���������. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ��������� ��������� ������� �����������.
    
## <a name="remarks"></a>Примечания

����� **IMsgStore::NotifyNewMail** ���������� ����������� ������� MAPI ��� ���������� ��������� ���������, ��� ��������� ������ ��� ��������. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

��� ������ **NotifyNewMail** ��������� ����������� � ��������� ����� ���� ������������������ �������������. ����� ��������� �����������, ������ [IMAPISupport::Notify](imapisupport-notify.md), ���� �� ������ ������������ ������ ������� ��������� ��� � ������� ����������� ����������. ������������������ �������� � ��� ���� � ������ [IMsgStore::Advise](imsgstore-advise.md) , ���������� ��� ���������  _lpEntryID_ �������� NULL, ��������  _ulEventMask_ ���  _fnevNewMail_. 
  
�� ��������� � �� ���������� ������ ��� ��������� [�����������](notification.md) � ��������� ����������� � ��������� �����. ���������� ��������� **NOTIFICATION**, ������ ��������������� ������� [ScCopyNotifications](sccopynotifications.md) , ����� ������������ �������� � ��� ������. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[�����������](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

