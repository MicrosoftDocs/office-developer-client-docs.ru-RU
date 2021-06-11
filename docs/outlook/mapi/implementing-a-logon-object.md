---
title: Реализация объекта Logon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433047"
---
# <a name="implementing-a-logon-object"></a>Реализация объекта Logon

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Каждая адресная книга, магазин сообщений и поставщик транспорта мгновенно передает объект logon в рамках реализации [IABProvider:::Logon,](iabprovider-logon.md) [IMSProvider::Logon](imsprovider-logon.md)или [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Объекты Logon реализуют методы, которые помогают запросам клиентов службы MAPI. В зависимости от типа поставщика услуг ваш объект logon будет поддерживать один из следующих интерфейсов. 
  
|**Интерфейс объекта Logon**|**Поставщик услуг**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Поставщик адресных книг  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Поставщик магазина сообщений  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Поставщик транспорта  <br/> |
   
Поставщики адресных книг и магазинов сообщений реализуют следующие функции в своих объектах с логотипом:
  
- Поддержка уведомлений о событиях **(рекомендации** и **методы unadvise).** Обзор уведомлений о событиях см. в [примере Event Notification in MAPI.](event-notification-in-mapi.md) Дополнительные сведения о поддержке уведомления в объекте logon см. в дополнительных сведениях [о поддержке уведомления о событиях.](supporting-event-notification.md) 
    
- Сравнение идентификатора входа **(метод CompareEntryIDs).** Общие сведения об идентификаторах входа см. в [документе MAPI Entry Identifiers.](mapi-entry-identifiers.md) Дополнительные сведения о сравнении идентификаторов записей в методе **CompareEntryIDs** объекта вашего логона см. в дополнительных сведениях о поддержке доступа к объекту [и сравнения.](supporting-object-access-and-comparison.md)
    
- Доступ к дополнительным сведениям об ошибках **(метод GetLastError).** Дополнительные сведения об обработке ошибок в MAPI см. в см. в [руб. Обработка ошибок в MAPI.](error-handling-in-mapi.md) 
    
- Доступ к объектам, реализованным поставщиком услуг **(метод OpenEntry).** Дополнительные сведения см. в [дополнительных сведениях о поддержке доступа к объектам и сравнения.](supporting-object-access-and-comparison.md)
    
- Доступ к объекту состояния **(метод OpenStatusEntry).** Общие сведения об объектах состояния см. в [mapi Status Objects.](mapi-status-objects.md) Конкретные сведения о реализации объекта состояния см. в этой [информации.](status-object-implementation.md)
    
- Процесс входа **(метод logoff).** Дополнительные сведения см. [в переключениях с поставщиком услуг.](shutting-down-a-service-provider.md)
    
Если ваш поставщик является поставщиком адресной книги, вы также будете внедрять следующие методы и связанные функции:
  
- [IABLogon::GetOneOffTable,](iablogon-getoneofftable.md) чтобы предоставить список шаблонов, которые вы поддерживаете для создания новых получателей. Дополнительные сведения см. в [таблице One-Off Tables](one-off-tables.md) или [Implementing a Provider One-Off Table.](implementing-a-provider-one-off-table.md)
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) для предоставления доступа к реализации получателя, данные которого находятся в поставщике хост-адресной книги. Дополнительные сведения см. [в книге Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P repareRecips,](iablogon-preparerecips.md) чтобы убедиться, что соответствующие свойства доступны для всех получателей в списке получателей. Дополнительные сведения см. [в iABLogon::P repareRecips.](iablogon-preparerecips.md) 
    
Объект логотипа поставщика транспорта, который реализует [IXPLogon : IUnknown,](ixplogoniunknown.md)сильно отличается от объектов logon, реализованных другими типами поставщиков услуг. Он имеет только две общие функции с другими объектами логотипа: доступ к объекту состояния с помощью [метода IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) и операция входа с помощью метода [IXPLogon::TransportLogoff.](ixplogon-transportlogoff.md) Поставщики транспорта реализуют следующие уникальные функции в своих объектах с логотипом: 
  
- Регистрация для типов адресов[(метод IXPLogon::AddressTypes).](ixplogon-addresstypes.md) Дополнительные сведения о регистрации типа адресов см. в примере [Transport Provider и MAPI Spooler Operational Model.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Управление передачей сообщений[(методы IXPLogon::StartMessage,](ixplogon-startmessage.md) [IXPLogon::EndMessage](ixplogon-endmessage.md)и [IXPLogon::SubmitMessage).](ixplogon-submitmessage.md) Дополнительные сведения см. в [примере "Модель](message-reception-model.md)приема сообщений", "Взаимодействие с [Spooler MAPI"](interacting-with-the-mapi-spooler.md)и ["Модель отправки сообщений".](message-submission-model.md)
    
- Внутренняя проверка состояния[(метод IXPLogon::ValidateState).](ixplogon-validatestate.md) 
    
- Возможность скачивания или отправки сообщений по запросу[(метод IXPLogon::FlushQueues).](ixplogon-flushqueues.md) Дополнительные сведения см. [в методе Implementing the FlushQueues.](implementing-the-flushqueues-method.md)
    
- Возможность запроса ожидающих сообщений[(метод IXPLogon::P ll).](ixplogon-poll.md) Дополнительные сведения см. в [примере Модели приема сообщений.](message-reception-model.md)
    
- Обнаружение состояния ожидания[(метод IXPLogon::Idle).](ixplogon-idle.md) 
    
- Взаимодействие с шпалером[MAPI (метод IXPLogon::TransportNotify).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>См. также



[Реализация logon поставщика услуг](implementing-service-provider-logon.md)

