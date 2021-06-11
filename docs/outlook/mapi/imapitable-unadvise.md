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
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода [IMAPITable::Advise.](imapitable-advise.md) 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Номер регистрационного подключения, возвращаемого вызовом [в IMAPITable::Advise.](imapitable-advise.md)
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> The call succeeded.
    
## <a name="remarks"></a>Примечания

Используйте метод **IMAPITable::Unadvise,** чтобы освободить указатель для объекта раковины рекомендации, переданного в  _параметре lpAdviseSink_ в предыдущем вызове **на IMAPITable:::Advise,** тем самым отменив регистрацию уведомлений. В рамках отбрасывания указателя к объекту раковины рекомендации используется метод **IUnknown::Release.** Как **правило,** выпуск вызывается во время вызова **Unadvise,** но если другой поток находится в процессе вызова [метода IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для раковины рекомендации, вызов выпуска откладывается до возвращения метода **OnNotify.**  
  
Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md) Сведения о уведомлении таблицы см. в [таблице Уведомлений.](about-table-notifications.md) Сведения об использовании методов **IMAPISupport** для поддержки уведомлений см. в сообщении [о поддержке событий.](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI использует **метод IMAPITable::Unadvise** для отмены уведомлений для таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

