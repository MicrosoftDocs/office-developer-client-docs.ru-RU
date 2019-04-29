---
title: Имапитаблеунадвисе
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода [IMAPITable:: Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _Улконнектион_
  
> возврата Номер подключения регистрации, возвращенный при вызове метода [IMAPITable:: Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> The call succeeded.
    
## <a name="remarks"></a>Примечания

Используйте метод **IMAPITable::** unadvise, чтобы освободить указатель на объект приемника уведомлений, переданный в параметре _лпадвисесинк_ при предыдущем вызове метода **IMAPITable:: Advise**, тем самым отменяя регистрацию уведомлений. При отмене указателя на объект приемника уведомлений вызывается метод " **IUnknown:: Release** " объекта. Как правило, **выпуск** вызывается во время вызова метода unadvise, но если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для приемника уведомлений, вызов **освобождения** задерживается, пока не будет задано значение **** OnNotify **** метод возвращает значение. 
  
Более подробную информацию о процессе уведомления можно узнать [в статье уведомление о событии в MAPI](event-notification-in-mapi.md). Конкретные сведения о табличных уведомлениях см [](about-table-notifications.md). Сведения о том, как использовать методы **имаписуппорт** для поддержки уведомлений, можно узнать в разделе [Поддержка уведомлений о событиях](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Контентстаблелистктрл. cpp  <br/> |Кконтентстаблелистктрл:: Нотификатионофф  <br/> |MFCMAPI использует метод **IMAPITable:: unadvise** для отмены уведомлений для таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

