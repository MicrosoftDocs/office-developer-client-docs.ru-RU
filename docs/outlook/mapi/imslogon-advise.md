---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317313"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует объект с поставщиком магазина сообщений для уведомлений об изменениях в хранилище сообщений. Затем хранилище сообщений отправляет уведомления об изменениях в зарегистрированном объекте.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Размер в bytes идентификатора записи, на который указывает _параметр lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа объекта, о котором должны быть созданы уведомления. Этот объект может быть папкой, сообщением или любым другим объектом в хранилище сообщений. Кроме того, если MAPI задает параметр  _cbEntryID_ до 0 и передает **null** для  _lpEntryID,_ раковина рекомендации предоставляет уведомления об изменениях во всем хранилище сообщений.
    
 _ulEventMask_
  
> [in] Маска событий типов событий уведомлений, происходящих для объекта, о котором MAPI будет генерировать уведомления. Маска фильтрует определенные случаи. Каждый тип события имеет связанную с ним структуру, которая содержит дополнительные сведения о событии. В следующей таблице перечислены возможные типы событий вместе с соответствующими структурами.
    
|**Тип события уведомлений**|**Соответствующая структура**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект помойки, который должен быть вызван, когда происходит событие для объекта сеанса, о котором было запрощено уведомление. Этот объект, рекомендуемый для раковины, уже должен существовать.
    
 _lpulConnection_
  
> [вышел] Указатель на переменную, которая после успешного возврата сохраняет номер подключения для регистрации уведомлений. Номер подключения должен быть незеро.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается MAPI или одним или более поставщиками услуг.
    
## <a name="remarks"></a>Примечания

Поставщики магазинов сообщений реализуют **метод IMSLogon::Advise** для регистрации объекта для отзовов уведомлений. Всякий раз, когда происходит изменение в указанный объект, поставщик проверяет, какой бит маски события был задан в  _параметре ulEventMask_ и, следовательно, какой тип изменения произошел. Если задан бит, поставщик вызывает [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта раковины рекомендации, указанный параметром  _lpAdviseSink_ для отчета о событии. Данные, переданные в структуре уведомлений в **режим OnNotify,** описывают событие. 
  
Вызов **OnNotify может** произойти во время вызова, который изменяет объект, или в любое более позднее время. В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке. Чтобы безопасно обрабатывать вызов **OnNotify,** который может произойти в неподходящий момент, клиентский приложение должно использовать функцию [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Для предоставления уведомлений поставщику магазина сообщений, который реализует **рекомендации,** необходимо сохранить копию указателя на _объект lpAdviseSink;_ Для этого поставщик вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для раковины рекомендации для поддержания указателя объекта до отмены регистрации уведомлений с вызовом метода [IMSLogon::Unadvise.](imslogon-unadvise.md) Реализация **Advise** должна назначить номер подключения для регистрации уведомлений и вызвать **AddRef** на этот номер подключения, прежде чем возвращать его в _параметре lpulConnection._ Поставщики служб могут освободить объект помойки рекомендации до отмены регистрации, но они не должны выпускать номер подключения до тех пор, пока не будет вызван **Unadvise.** 
  
После успешного  вызова в Службу консультирования и до вызова **Unadvise** необходимо подготовить поставщиков для выпуска объекта раковины рекомендации. Таким образом, поставщик должен освободить свой  объект раковины рекомендации после рекомендации возвращает, если он не имеет определенного долгосрочного использования для него. 
  
Дополнительные сведения о процессе уведомления см. в сообщении [события в MAPI.](event-notification-in-mapi.md) 
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[�����������](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

