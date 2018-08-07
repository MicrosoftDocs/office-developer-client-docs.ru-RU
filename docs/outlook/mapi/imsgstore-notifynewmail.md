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
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Относится к**: Outlook 
  
����������� ��������� ���������, ����� ���������. ���� ����� ���������� ������ ����������� ������� MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>���������

 _lpNotification_
  
> [in] ��������� �� ��������� [�����������](notification.md) � ��������� ����������� � ��������� ���������. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ��������� ��������� ������� �����������.
    
## <a name="remarks"></a>���������

����� **IMsgStore::NotifyNewMail** ���������� ����������� ������� MAPI ��� ���������� ��������� ���������, ��� ��������� ������ ��� ��������. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

��� ������ **NotifyNewMail** ��������� ����������� � ��������� ����� ���� ������������������ �������������. ����� ��������� �����������, ������ [IMAPISupport::Notify](imapisupport-notify.md), ���� �� ������ ������������ ������ ������� ��������� ��� � ������� ����������� ����������. ������������������ �������� � ��� ���� � ������ [IMsgStore::Advise](imsgstore-advise.md) , ���������� ��� ���������  _lpEntryID_ �������� NULL, ��������  _ulEventMask_ ���  _fnevNewMail_. 
  
�� ��������� � �� ���������� ������ ��� ��������� [�����������](notification.md) � ��������� ����������� � ��������� �����. ���������� ��������� **NOTIFICATION**, ������ ��������������� ������� [ScCopyNotifications](sccopynotifications.md) , ����� ������������ �������� � ��� ������. 
  
## <a name="see-also"></a>��. �����



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[�����������](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

