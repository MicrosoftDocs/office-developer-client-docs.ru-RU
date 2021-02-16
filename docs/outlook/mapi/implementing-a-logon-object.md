---
title: Реализация объекта logon
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
# <a name="implementing-a-logon-object"></a>Реализация объекта logon

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Каждая адресная книга, хранилище сообщений и поставщик транспорта в процессе реализации [IABProvider::Logon,](iabprovider-logon.md) [IMSProvider::Logon](imsprovider-logon.md)или [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)мгновенно и мгновенно представляет объекты, которые можно использовать. Объекты для логотипа реализуют методы, которые помогают запросам клиента службы MAPI. В зависимости от типа поставщика услуг ваш объект для логотипа будет поддерживать один из следующих интерфейсов. 
  
|**Интерфейс объекта Logon**|**Поставщик услуг**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Поставщик адресной книги  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Поставщик службы хранения сообщений  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Поставщик транспорта  <br/> |
   
Поставщики адресной книги и магазина сообщений реализуют следующие функции в своих объектах для логотипа:
  
- Поддержка уведомлений о событиях (**методы advise** и **Unadvise).** Обзор уведомления о событии см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) Дополнительные сведения о поддержке уведомлений в объекте для логотипа см. в соответствующем [уведомлении.](supporting-event-notification.md) 
    
- Сравнение идентификаторов записей (**метод CompareEntryIDs).** Общие сведения об идентификаторах записей см. в документе [MAPI Entry Identifiers.](mapi-entry-identifiers.md) Дополнительные сведения о сравнении идентификаторов записей в методе **CompareEntryIDs** объекта входа см. в вспомогательных методах "Доступ к объектам" [и "Сравнение".](supporting-object-access-and-comparison.md)
    
- Доступ к дополнительным сведениям об ошибках (**метод GetLastError).** Дополнительные сведения об обработке ошибок в MAPI см. в [этой теме.](error-handling-in-mapi.md) 
    
- Доступ к объектам, реализованным поставщиком услуг (метод **OpenEntry).** Дополнительные сведения см. в [дополнительных сведениях о поддержке доступа к объектам и сравнения.](supporting-object-access-and-comparison.md)
    
- Доступ к объекту состояния (**метод OpenStatusEntry).** Общие сведения об объектах состояния см. в поддоме ["Объекты состояния MAPI".](mapi-status-objects.md) Конкретные сведения о реализации объекта состояния см. в [реализации объекта status.](status-object-implementation.md)
    
- Процесс выйдите из систему **(метод Logoff).** Дополнительные сведения см. в сведениях [о закрытии поставщика услуг.](shutting-down-a-service-provider.md)
    
Если ваш поставщик является поставщиком адресной книги, также реализуются следующие методы и связанные функции:
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) для предоставления списка шаблонов, поддерживаемых для создания новых получателей. Дополнительные сведения см. в [таблицах one-off или](one-off-tables.md) [Implementing a Provider One-Off Table.](implementing-a-provider-one-off-table.md)
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) для предоставления доступа к реализации получателя, данные которого находятся в поставщике адресной книги хост-адреса. Дополнительные сведения [см. в под вопросе "Действующие как поставщик внешних адресных книг".](acting-as-a-foreign-address-book-provider.md) 
    
- [IABLogon::P repareRecips,](iablogon-preparerecips.md) чтобы убедиться, что соответствующие свойства доступны для всех получателей в списке получателей. Дополнительные сведения см. в [IABLogon::P repareRecips.](iablogon-preparerecips.md) 
    
Объект для логотипа поставщика транспорта, который реализует [IXPLogon : IUnknown,](ixplogoniunknown.md)сильно отличается от объектов для логотипа, реализованных другими типами поставщиков услуг. У него есть только две общие функции с другими объектами входа: доступ к объекту состояния с помощью метода [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) и операция выйдите из системы с помощью метода [IXPLogon::TransportLogoff.](ixplogon-transportlogoff.md) Поставщики транспорта реализуют следующие уникальные функции в своих объектах для логотипа: 
  
- Регистрация для типов адресов ([метод IXPLogon::AddressTypes).](ixplogon-addresstypes.md) Дополнительные сведения о регистрации типа адреса см. в сведениях о поставщике транспорта и операционной модели пула [MAPI.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Управление передачей сообщений ([методы IXPLogon::StartMessage,](ixplogon-startmessage.md) [IXPLogon::EndMessage](ixplogon-endmessage.md)и [IXPLogon::SubmitMessage).](ixplogon-submitmessage.md) Дополнительные сведения см. в модели приема [сообщений,](message-reception-model.md)взаимодействии с [пулом MAPI](interacting-with-the-mapi-spooler.md)и [модели отправки сообщений.](message-submission-model.md)
    
- Внутренняя проверка состояния ([метод IXPLogon::ValidateState).](ixplogon-validatestate.md) 
    
- Возможность скачивать или отправлять сообщения по запросу ( метод[IXPLogon::FlushQueues).](ixplogon-flushqueues.md) Дополнительные сведения [см. в окне "Реализация метода FlushQueues".](implementing-the-flushqueues-method.md)
    
- Возможность запрашивать ожидающих сообщений ( метод[IXPLogon::P oll).](ixplogon-poll.md) Дополнительные сведения см. в модели [приема сообщений.](message-reception-model.md)
    
- Обнаружение состояния бездействия ([метод IXPLogon::Idle).](ixplogon-idle.md) 
    
- Взаимодействие с пулером MAPI ([метод IXPLogon::TransportNotify).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>См. также



[Реализация службы для логоса](implementing-service-provider-logon.md)

