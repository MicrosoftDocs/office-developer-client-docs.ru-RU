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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отвечает на уведомление, выполняя одну или несколько задач. Выполняемые задачи зависят от типа события и объекта, который создает уведомление. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameters

 _cNotif_
  
> [in] Количество структур [УВЕДОМЛЕНий,](notification.md) на которые указывает параметр _lpNotifications._ 
    
 _lpNotifications_
  
> [in] Указатель на одну или несколько **структур УВЕДОМЛЕНий,** которые предоставляют сведения о произошедших событиях. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление было успешно обработано.
    
## <a name="remarks"></a>Примечания

Процесс уведомления начинается, когда клиент или MAPI делает  вызов методу консультирования поставщика услуг для регистрации для получения уведомления определенного типа для определенного объекта. Один из параметров метода **Advise** — указатель на объект раковины, который реализует [интерфейс IMAPIAdviseSink.](imapiadvisesinkiunknown.md) Если событие происходит с целевым объектом, соответствующим зарегистрированным уведомлениям, поставщик услуг прямо или косвенно через MAPI вызывает метод **OnNotify** раковины рекомендации. 
  
Вызов **OnNotify может** произойти во время вызова MAPI, вызываемом событием, или в более позднее время. В системах, поддерживаюх несколько потоков выполнения, **OnNotify** можно назвать как по одному потоку, который использовался для регистрации, так и по другому потоку. Клиенты могут убедиться, что вызов **OnNotify** выполнен  на том же потоке,  который используется для вызова "Советы", создав раковину рекомендации, которую они передают в консультацию с функцией [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Параметр  _lpNotifications_ указывает на одну или несколько структур **УВЕДОМЛЕНий,** которые описывают изменения во время события. Существует другой тип структуры **УВЕДОМЛЕНий** для каждого типа события. 
  
В следующей таблице перечислены значения, которые используются для представления возможных типов событий и структур, связанных с каждым значением:
  
|**Тип события уведомлений**|**Соответствующая структура**|
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
   
Дополнительные сведения о том, как настроить и остановить уведомления, см. в справочных записях методов Advise **и** **Unadvise** для любого из следующих интерфейсов: [IABLogon,](iablogoniunknown.md) [IAddrBook,](iaddrbookimapiprop.md) [IMAPIForm, IMAPISession,](imapisessioniunknown.md) [IMAPITable,](imapitableiunknown.md) [](imapiformiunknown.md) [IMsgStore](imsgstoreimapiprop.md)и [IMSLogon](imslogoniunknown.md). 
  
Общие сведения о процессе уведомления см. в сообщении [о событиях в MAPI.](event-notification-in-mapi.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **OnNotify** обычно состоит из одного или нескольких блоков кода для каждого типа уведомлений, которые вы ожидаете получить. В этих блоках кода выполните любые задачи, которые вы считаете необходимыми в качестве ответа на уведомление. Например, предположим, что вы регистрируете для получения **уведомлений fnevObjectModified** в папке, которая включена в диалоговое окно. В блоке кода, который вы включаете в метод **OnNotify** для обработки уведомлений **fnevObjectModified,** можно отправить Windows в диалоговое окно для запроса обновленного отображения. 
  
Не изменять или освободить структуру **УВЕДОМЛЕНий,** переданную **OnNotify.** Данные в структуре действительны только до тех пор, пока **OnNotify** не вернется. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При внесении изменений в несколько объектов можно уведомить зарегистрированную раковину рекомендации в одном вызове **OnNotify** или в нескольких вызовах в зависимости от ограничений памяти. Это верно независимо от того, являются ли изменения результатом одного или нескольких вызовов метода. Например, вызов в [IMAPIFolder::CopyMessages может](imapifolder-copymessages.md) повлиять на несколько сообщений и папок. В качестве поставщика магазина сообщений можно сделать один вызов **onNotify** с типом **событий fnevObjectModified** для целевой папки или множеством вызовов, по одному для каждого затрагиваемого сообщения. Аналогично, если клиент совершает повторные вызовы [в IMAPIFolder::CreateMessage,](imapifolder-createmessage.md)эти вызовы можно объединить в одно **событие fnevObjectModified** для папки или разделить на отдельные **события fnevObjectCreated** для каждого нового сообщения. 
  
Дополнительные сведения о том, как и когда создавать уведомления, см. в дополнительных сведениях Об уведомлении о событиях в [MAPI](event-notification-in-mapi.md) и [вспомогательном уведомлении о событиях.](supporting-event-notification.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AdviseSink.h и AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |Класс CAdviseSink реализуется для обработки всех уведомлений в MFCMAPI.  <br/> |
   
## <a name="see-also"></a>См. также



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�����������](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

