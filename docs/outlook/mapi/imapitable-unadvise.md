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
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMAPITable::Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Число подключений к регистрации, возвращаемых вызовом [IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> The call succeeded.
    
## <a name="remarks"></a>Замечания

Используйте метод **IMAPITable::Unadvise** для освобождения указатель на объект приемника уведомлений, переданной в параметре _lpAdviseSink_ в предыдущем вызове **IMAPITable::Advise**, тем самым Отмена регистрации уведомлений. Как часть пропуск указатель на объект приемника уведомлений вызывается метод **функции IUnknown::Release** объекта. Как правило, называется **выпуска** во время вызова **Unadvise** , но если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для приемник уведомлений вызова **выпуске** откладывается до **OnNotify** метод возвращает. 
  
Дополнительные сведения о процессе уведомления видеть [Уведомления о событии в MAPI](event-notification-in-mapi.md). Сведения о таблице уведомлений содержатся [Уведомления о таблице](about-table-notifications.md). Сведения об использовании методов **IMAPISupport** для поддержки уведомлений [Поддерживающие уведомления о событии](supporting-event-notification.md)см.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |Mfcmapi (en) использует метод **IMAPITable::Unadvise** для отмены уведомления для таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

