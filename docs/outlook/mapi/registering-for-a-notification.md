---
title: Регистрация для уведомления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424905"
---
# <a name="registering-for-a-notification"></a>Регистрация для уведомления

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиент может зарегистрироваться для уведомлений адресной книги или из магазина сообщений в процессе инициализации.
  
MAPI поддерживает уведомление в адресной книге независимо от того, поддерживает ли ее какой-либо поставщик адресной книги. Поддержка уведомлений в хранилищах сообщений зависит от конкретного поставщика хранилища сообщений. Чтобы определить, поддерживает ли конкретный поставщик хранилищ сообщений уведомления, проверьте его PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md) Если хранилище сообщений поддерживает уведомления, STORE_NOTIFY_OK бит. 
  
Зарегистрируйтесь для получения уведомлений, вызывая метод advise source object's **Advise.** Многие объекты **реализуют advise,** и клиенты могут регистрироваться в этих объектах различными способами. 
  
 **Регистрация уведомления**
  
1. Создайте объект -источник рекомендации MAPI и приумножйте его количество ссылок.
    
2. При необходимости вызовите [HrThisThreadAdviseSink,](hrthisthreadadvisesink.md) чтобы создать объект-замещений, который будет обтекать исходный тоник рекомендаций, а затем отпустите исходный тоник советов. 
    
3. Вызовите один из следующих методов **advise** для завершения регистрации: 
    
  - Call [IMAPISession::Advise](imapisession-advise.md) to register for session notifications or for notifications on an address book or message store object. 
    
  - Call [IAddrBook::Advise](iaddrbook-advise.md) to register for address book notifications or for notifications on a messaging user, container, or distribution list. 
    
  - Call [IABLogon::Advise](iablogon-advise.md) to register directly with an address book provider for notifications on a messaging user, container, or distribution list. 
    
  - Call [IMsgStore::Advise](imsgstore-advise.md) to register for message store notifications or for notifications on a folder or message. 
    
  - Call [IMSLogon::Advise](imslogon-advise.md) to register directly with a message store provider for notifications on a folder or message. 
    
  - Call [IMAPITable::Advise](imapitable-advise.md) to register for table notifications. 
    
4. Кэшйте номер подключения, возвращенный **из** advise .
    
5. Если используется оболочка, выпустите ее. После регистрации оболочки сконсультируйтесь, она вам больше не понадобится.
    
Calling ** IMAPISession::Advise ** enables you to register for critical error notifications on the overall session or for various notifications on individual objects. Сеансы отправляют критические уведомления об ошибках клиентам, войдите в общие сеансы, когда другой клиент, использующий общий сеанс, вызывает метод [IMAPISession::Logoff.](imapisession-logoff.md) Чтобы зарегистрироваться для уведомлений сеанса, передав NULL для параметра идентификатора записи. Чтобы зарегистрировать уведомления для отдельного объекта, передав идентификатор записи объекта. Метод **IMAPISession** передает вызов соответствующему поставщику услуг, как определяется **частью MAPIUID** идентификатора записи. Вызов **метода IMAPISession::Advise** для регистрации уведомлений об объектах проще, чем вызов метода **Advise** поставщика услуг. 
  
Регистрация в адресной книге аналогична регистрации в сеансе. Чтобы зарегистрировать уведомление о критической ошибке из адресной книги, передав NULL для идентификатора записи. Чтобы зарегистрироваться для уведомлений в определенном объекте адресной книги, укажите соответствующий идентификатор записи, а также события или события, интересующие вас. Следует помнить, что многие поставщики адресных книг не поддерживают уведомления по отдельным объектам. Вместо этого они поддерживают уведомления таблиц в их содержимом и таблицах иерархии. 
  
Рекомендуем освободить обойму, которую вы реализуете или создаете с помощью [HrAllocAdviseSink,](hrallocadvisesink.md) сразу же после успешного возврата после вызова **advise.** Это возможно, так как поставщики услуг могут освободить  ваш сигнал консультации после вызова "Сообщить", но до вызова **Unadvise.** После того как вы надали источнику консультации указатель на ваш обойма, а количество ссылок на него было бы больше, лучше освободить его, если вы не используете его в долгосрочной перспективе. 
  
> [!NOTE]
> Все номера подключений, которые представляют действительные регистрации рекомендаций, не будут отпущены до тех пор, пока не будет выполнен вызов **Unadvise.** 
  

