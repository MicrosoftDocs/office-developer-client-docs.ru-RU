---
title: Идентификаторы адресных книг
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0814d76dac97e40940f41c49dbf72efdd26b3cca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808018"
---
# <a name="address-book-identifiers"></a>Идентификаторы адресных книг

  
  
**Относится к**: Outlook 
  
Все поставщиками адресной книги назначьте идентификаторы записей с помощью свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) для имени пользователя обмена мгновенными сообщениями и объекты списка рассылки. Клиентские приложения используйте следующие идентификаторы записей для открытия и доступа к объектам, к которым они назначены.
  
В адресной книге используются три типа идентификаторов для представления объектов:
  
- Идентификаторы единичных записей
    
- Идентификаторы записей одноразовых шаблона
    
- Идентификаторы шаблона
    
Из-за различных подобия, с которым они имеют имена и идентификаторы записей можно легко стать знаю, как использовать и создается каждого типа. 
  
Идентификатор единичных записей — это идентификатор записи, который используется для открытия и получить доступ к тип получателя, известных как одного раза или настраиваемые получателя. One-offs являются получателей, которые не принадлежат какие-либо поставщиками адресной книги в профиле. Идентификаторы записей, назначенный one-offs использовать формат специально зарезервировано для одноразовых получателей. Так как идентификаторы единичных записей используются для открытия и доступа к объектам, они сохраняются в свойстве PR_ENTRYID.
  
Создаются One-offs и идентификаторы единичных записей:
  
- Когда пользователи из клиентского приложения выбрать добавить получателя в список получателей сообщения не представляют все записи в адресной книге.
    
- Когда пользователи из клиентского приложения по своему выбору добавить получателя, который не представляют все записи в адресной книге в контейнер изменяемые адресной книги.
    
- Когда поставщика транспорта получает сообщение с адреса, который не может справиться с его поставщик связанных с ними адресной книги.
    
- Когда поставщика транспорта получает сообщение с адресом, который относится к шлюзу.
    
В первых двух случаях клиент вызывает **IAddrBook::CreateOneOff** для сопоставления идентификатора единичных записей с только что созданный одноразовых получателя. В следующие две ситуации поставщика транспорта вызывает **IMAPISupport::CreateOneOff** для сопоставления идентификатора единичных записей на внешний адрес. Для получения дополнительных сведений см [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) и [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Идентификатор записи одноразовых шаблона является краткосрочной идентификатор записи, которая используется для открытия и доступа к шаблон для создания one-offs. Поставщиками адресной книги и MAPI использовать шаблоны для ввода сведения, необходимые для создания определенного типа получателя. Сведения об этих шаблонов, включая их идентификаторы записей публикуется в одноразовых таблице. Одноразовых таблиц при MAPI вызывает метод **IABLogon::GetOneOffTable** или метод **IMAPIProp::OpenProperty** контейнер адресной книги для запроса **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) свойство или когда поставщик вызывает метод **IMAPISupport::GetOneOffTable**. Для получения дополнительных сведений см [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)и [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Чтобы создать новый раза, пользователь выбирает один из шаблонов, перечисленные в таблице одноразовых. Клиент передает в столбце PR_ENTRYID из выбранную строку, которая идентификатор записи одноразовых шаблон выбранного шаблона, **IAddrBook::NewEntry** с помощью параметра _lpEIDNewEntryTpl_ . Для получения дополнительных сведений см [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI используется идентификатор записи одноразовых шаблона для отображения шаблона и разрешает пользователю введите сведения, необходимые для создания получателя. 
  
Идентификатор шаблона — это идентификатор входа, некоторые поставщиками адресных книг по их получателей в дополнение к идентификатор записи, которая хранится в свойстве PR_ENTRYID. Поставщики свойства получателя **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) для хранения идентификатору шаблона. Некоторые поставщиками адресных книг назначение такое же значение для свойства запись идентификатор и идентификатор шаблона получателя.
  
Шаблон идентификаторов используются только с поставщиками адресной книги и по MAPI для привязки данные получателей в один поставщик, называется поставщик узла на код для получателя в другой поставщик, называется внешнего поставщика. Поставщик узла предоставляет хранилище для получателя; внешний поставщик логику. Процесс привязки позволяет обновлять данные получателя хранятся с использованием кода внешнего поставщика этот поставщик.
  
Когда поставщик узла будет готов для изменения ее получателя, свойство PR_TEMPLATEID передается в вызов метода **IMAPISupport::OpenTemplateID** для запуска процесса привязки. MAPI продолжит процесс путем передачи идентификатора шаблона для соответствующего внешнего поставщика путем вызова метода **IABLogon::OpenTemplateID** . Для получения дополнительных сведений см [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) и [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). Внешний поставщик возвращает указатель на его реализация **IMAPIProp** для получателя, который поставщик узла можно использовать вместо собственная реализация. 
  
