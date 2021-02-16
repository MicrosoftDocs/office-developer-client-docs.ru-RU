---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407363"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отвечает на уведомление, выполняя одну или несколько задач. Выполняемые задачи зависят от типа события и объекта, который создает уведомление. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Параметры

 _cNotif_
  
> [in] Количество структур [УВЕДОМЛЕНий,](notification.md) на которые указывает параметр _lpNotifications._ 
    
 _lpNotifications_
  
> [in] Указатель на одну  или несколько структур УВЕДОМЛЕНий, которые предоставляют сведения о произошедших событиях. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно обработано.
    
## <a name="remarks"></a>Примечания

Процесс уведомления начинается, когда клиент или MAPI совершает  вызов метода Advise поставщика услуг для регистрации для получения уведомления определенного типа для конкретного объекта. Одним из параметров метода **Advise** является указатель на объект приемника рекомендации, который реализует интерфейс [IMAPIAdviseSink.](imapiadvisesinkiunknown.md) Когда происходит событие для целевого объекта, соответствующего зарегистрированным уведомлениям, поставщик услуг напрямую или косвенно через MAPI вызывает метод **OnNotify** приемника рекомендации. 
  
Вызов **OnNotify может** произойти либо во время вызова MAPI, который вызывает событие, либо позднее. В системах, поддерживаюх несколько потоков выполнения, **OnNotify** можно назвать в одном потоке, который использовался для регистрации, или в другом потоке. Клиенты могут убедиться, что вызов **OnNotify** выполнен  в том же потоке,  который используется для вызова "Консультация", создав поток консультаций, который они передают в "Консультацию" с помощью функции [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Параметр  _lpNotifications_ указывает на одну или несколько структур **NOTIFICATION,** которые описывают изменения во время события. Для каждого типа события **существует** разный тип структуры УВЕДОМЛЕНий. 
  
В следующей таблице перечислены значения, используемые для представления возможных типов событий, и структуры, связанные с каждым значением:
  
|**Тип события notification**|**Соответствующая структура**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevNewMail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
Дополнительные сведения о том, как настроить и остановить уведомления, см. в справочных записях для методов **Advise** и **Unadvise** для любого из следующих интерфейсов: [IABLogon,](iablogoniunknown.md) [IAddrBook,](iaddrbookimapiprop.md) [IMAPIForm,](imapiformiunknown.md) [IMAPISession,](imapisessioniunknown.md) [IMAPITable,](imapitableiunknown.md) [IMsgStore](imsgstoreimapiprop.md)и [IMSLogon](imslogoniunknown.md). 
  
Общие сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **OnNotify** обычно состоит из одного или нескольких блоков кода для каждого типа уведомлений, которые вы ожидаете получить. В этих блоках кода выполните все задачи, которые вы считаете необходимыми в качестве ответа на уведомление. Например, предположим, что вы регистрируете получение уведомлений **fnevObjectModified** для папки, включенной в диалоговое окно. В блоке кода, который вы включаете в метод **OnNotify** для обработки уведомлений **fnevObjectModified,** вы можете отправить сообщение Windows в диалоговое окно, чтобы запросить обновленное отображение. 
  
Не изменяйте или не освободийте **структуру** УВЕДОМЛЕНий, переданную **в OnNotify.** Данные в структуре действительны только до тех пор, пока **OnNotify** не возвратит данные. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При внесении изменений в несколько объектов вы можете уведомить зарегистрированный коннект-конюхс в одном вызове **OnNotify** или при нескольких вызовах в зависимости от ограничений памяти. Это справедливо независимо от того, являются ли изменения результатом одного вызова метода или нескольких методов. Например, вызов [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) может повлиять на несколько сообщений и папок. Как поставщик службы хранения сообщений вы можете один вызов **OnNotify** с типом события **fnevObjectModified** для целевой папки или множеством вызовов, по одному для каждого из них, влияющих на сообщения. Аналогично, если клиент совершает повторные вызовы [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md)эти вызовы можно объединить в одно **событие fnevObjectModified** для папки или разделить на отдельные события **fnevObjectCreated** для каждого нового сообщения. 
  
Дополнительные сведения о том, как и когда создавать уведомления, см. в уведомлениях о событиях [MAPI](event-notification-in-mapi.md) и [вспомогательных уведомлениях о событиях.](supporting-event-notification.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AdviseSink.h и AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |Класс CAdviseSink реализован для обработки всех уведомлений в MFCMAPI.  <br/> |
   
## <a name="see-also"></a>См. также



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�����������](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

