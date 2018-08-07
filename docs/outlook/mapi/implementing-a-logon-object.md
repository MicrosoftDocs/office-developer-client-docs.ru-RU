---
title: Реализация объекта входа
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809288"
---
# <a name="implementing-a-logon-object"></a>Реализация объекта входа

  
  
**Относится к**: Outlook 
  
Каждые адресной книги, хранилища сообщений и поставщика транспорта создает экземпляр объекта входа в систему как часть своей реализации [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)или [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Объекты входа реализовать методы, которые помогают запросов клиентов MAPI службы. В зависимости от типа поставщика услуг объект входа в систему будет поддерживать один из следующих интерфейсов. 
  
|**Интерфейс входа в объект**|**Поставщик услуг**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Поставщик адресной книги  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Поставщик хранилища сообщений  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Поставщик транспорта  <br/> |
   
Адресная книга и сообщение внедряемые поставщиками хранилищ следующие функции в их объектами входа:
  
- Поддержка для уведомлений о событиях (методы**уведомлений** и **Unadvise** ). Обзор уведомлений о событиях в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). Дополнительные сведения о поддержке уведомлений в объекте входа видеть [Поддержка уведомления о событии](supporting-event-notification.md). 
    
- Сравнение идентификатор записи (метод**CompareEntryIDs** ). Общие сведения об идентификаторах запись [Идентификаторы MAPI записей](mapi-entry-identifiers.md)см. Дополнительные сведения о сравнении идентификаторы записей в метод **CompareEntryIDs** объекта входа можно [Поддержка доступа к объектам и сравнения](supporting-object-access-and-comparison.md).
    
- Доступ к Дополнительные сведения об ошибке (**GetLastError** метод). Дополнительные сведения об обработке ошибок в MAPI можно [Обработки ошибок в MAPI](error-handling-in-mapi.md). 
    
- Доступ к объектам, реализованные поставщиком услуг (**OpenEntry** метод). Для получения дополнительных сведений см [Поддержка доступа к объектам и сравнения](supporting-object-access-and-comparison.md).
    
- Доступ к объекту состояния (**OpenStatusEntry** метод). Общие сведения о состоянии объекты видеть [Состояние объектов MAPI](mapi-status-objects.md). Сведения о реализации объекта состояния содержатся [Реализация объекта состояния](status-object-implementation.md).
    
- Процесс выхода из системы (метод**Выход из системы** ). Для получения дополнительных сведений см [Завершает работу поставщика услуг](shutting-down-a-service-provider.md).
    
Если ваш поставщик поставщика адресных книг, следует также реализовать следующие методы и связанные функции:
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) предоставляет набор шаблонов, которые поддерживают для создания новых получателей. Для получения дополнительных сведений см [Одноразовых таблицы](one-off-tables.md) или [реализации поставщика одноразовых таблицы](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) для предоставления доступа к реализации получателя, данные которого находится в адресной книге узла. Для получения дополнительных сведений см [используется в качестве внешнего поставщик адресной книги](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::PrepareRecips](iablogon-preparerecips.md) убедитесь, что соответствующие свойства доступны для всех получателей в список получателей. Для получения дополнительных сведений см [IABLogon::PrepareRecips](iablogon-preparerecips.md). 
    
Объект входа поставщика транспорта, который реализует [IXPLogon: IUnknown](ixplogoniunknown.md), отличается от объектов входа в систему, реализованных других типов поставщиков услуг. Имеется только две возможности вместе с другими объектами входа: доступ к объекту состояния через метод [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) и операцию выхода из системы с помощью метода [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) . Поставщики транспорта реализации следующих уникальных функций в их объектами входа: 
  
- Регистрация типов адресов (метод[IXPLogon::AddressTypes](ixplogon-addresstypes.md) ). Дополнительные сведения о регистрации тип адреса можно [поставщика транспорта и модель действующие очереди MAPI](transport-provider-and-mapi-spooler-operational-model.md).
    
- Элемент управления передачи сообщений (методы[IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)и [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) ). Для получения дополнительных сведений см [Модели приема сообщений](message-reception-model.md), [Interacting с очередью MAPI](interacting-with-the-mapi-spooler.md)и [Модель отправки сообщения](message-submission-model.md).
    
- Проверка внутреннего состояния ([IXPLogon::ValidateState](ixplogon-validatestate.md) метод). 
    
- Возможность загрузки или отправки сообщений по запросу (метод[IXPLogon::FlushQueues](ixplogon-flushqueues.md) ). [Метод FlushQueues](implementing-the-flushqueues-method.md)для получения дополнительных сведений см.
    
- Возможность запроса для ожидающих сообщений (метод[IXPLogon::Poll](ixplogon-poll.md) ). Для получения дополнительных сведений см. [Модель приема сообщений](message-reception-model.md).
    
- Определение состояния простоя (метод[IXPLogon::Idle](ixplogon-idle.md) ). 
    
- Взаимодействие с очередью MAPI (метод[IXPLogon::TransportNotify](ixplogon-transportnotify.md) ). 
    
## <a name="see-also"></a>См. также



[Реализация входа для поставщика службы](implementing-service-provider-logon.md)

