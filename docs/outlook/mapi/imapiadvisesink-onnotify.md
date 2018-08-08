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
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808812"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**Относится к**: Outlook 
  
Отвечает на уведомление при выполнении одного или нескольких задач. Задачи, выполняемые зависят от типа события и объект, который создает уведомления. 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Параметры

 _cNotif_
  
> [in] Количество [УВЕДОМЛЕНИЙ](notification.md) структуры, на который указывает параметр _lpNotifications_ . 
    
 _lpNotifications_
  
> [in] Указатель на один или несколько **УВЕДОМЛЕНИЙ** структуры, содержащие сведения о событиях, которые происходили. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление обработан успешно.
    
## <a name="remarks"></a>Замечания

Уведомление процесс запускается после клиента или MAPI вызывает метод **уведомлений** поставщика услуг для получения уведомлений для определенного объекта определенного типа. Один из параметров для метода **уведомлений** является указатель на объект приемника уведомлений, который реализует интерфейс [IMAPIAdviseSink](imapiadvisesinkiunknown.md) . Когда возникает событие целевой объект, который соответствует зарегистрированного уведомления поставщика услуг, прямо или косвенно через MAPI, вызывает метод **OnNotify** приемник уведомлений. 
  
Вызов **OnNotify** может возникнуть во время вызова MAPI, который вызывает событие или позднее. На компьютерах, поддерживающих многопоточной среде **OnNotify** может быть вызван в том же потоке, который использовался для регистрации или в другом потоке. Клиенты могут убедитесь в том, что **OnNotify** вызов же потока, используемый для вызова **уведомлений** , создав приемник уведомлений, который они передать **уведомлений** с помощью функции [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Параметр _lpNotifications_ указывает одного или нескольких структур **УВЕДОМЛЕНИЙ** , которые описывают, что был изменен во время события. Существует другой тип структуры **УВЕДОМЛЕНИЙ** для каждого типа события. 
  
В следующей таблице приведены значения, используемые для представления возможных типов событий и структур, связанные с каждым из значений:
  
|**Тип события уведомления**|**Соответствующий структуры**|
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
   
Дополнительные сведения о том, как настроить и остановите уведомлений просмотра операций ссылку для **уведомлений** и **Unadvise** методов для каких-либо следующие интерфейсы: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)и [IMSLogon](imslogoniunknown.md). 
  
Общие сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **OnNotify** обычно будет состоять из одного или нескольких блоков кода для каждого типа согласно прогнозу, будут получать уведомления. В этих блоках кода выполнения задач, которые необходимо учитывать необходимые как ответ на уведомление. Например предположим, что Зарегистрируйтесь для получения уведомлений о **fnevObjectModified** на папку, включенную в поле показано диалоговое окно. В блоке кода, включение в методе **OnNotify** для обработки уведомлений **fnevObjectModified** может отправить сообщение Windows к диалоговому окну, чтобы запросить обновленные отображения. 
  
Не изменяйте и не освободить структура **УВЕДОМЛЕНИЙ** , переданной в **OnNotify**. Данные в структуре действителен только в том случае, пока возвращает **OnNotify** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При внесении изменений в несколько объектов, может уведомлять приемник зарегистрированных уведомлений в одном вызове **OnNotify** или в различных вызовов в зависимости от доступной памяти. Это значение true, независимо от того, является ли изменения, в результате вызова метода один или несколько. Например вызов [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) могут повлиять на нескольких сообщений и папок. Как поставщик хранилища сообщений можно сделать один вызов **OnNotify** с типом событий **fnevObjectModified** для целевой папке или много вызовов, другая — для каждого сообщения влияет. Аналогично Если клиент создает повторяющиеся вызовы [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), эти вызовы можно объединены в одно событие **fnevObjectModified** для папки или разделить на отдельные **fnevObjectCreated** событий для каждого нового сообщения. 
  
Дополнительные сведения о том, как и когда следует создавать уведомления в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md) и [Поддержка уведомлений о событиях](supporting-event-notification.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|AdviseSink.h и AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |Класс CAdviseSink реализуется для обработки всех уведомлений в mfcmapi (en).  <br/> |
   
## <a name="see-also"></a>См. также



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�����������](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

