---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d9235da7e7ec6ec244ee1a75f4795e9c77ec28bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579951"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициирует передачи входящих сообщений от поставщика транспорта диспетчер очереди MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpMessage_
  
> [in] Указатель на объект message (представляющий входящее сообщение), которая имеет разрешение чтения и записи, используемой поставщика транспорта для доступа и работы с этого сообщения. Этот объект действителен до после поставщика транспорта возвращает от вызова **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [out] Указатель на ссылку значение, присваиваемое сообщения. Диспетчер очереди MAPI инициализирует это значение 1, перед возвращает указатель на поставщика транспорта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Диспетчер очереди MAPI вызывает метод **IXPLogon::StartMessage** , чтобы начать передачу входящее сообщение от поставщика транспорта диспетчер очереди MAPI. Перед началом поставщика транспорта для использования сообщение, которое указывает _lpMessage_, следует хранить Справочник по сообщениям с помощью параметра _lpulMsgRef_ для возможности использования путем вызова метода [IXPLogon::TransportNotify](ixplogon-transportnotify.md) . 
  
Во время звонка **StartMessage** диспетчер очереди MAPI обрабатывает методы для объектов, открытых во время передачи сообщения, и он также обрабатывает все вложения. В этом обработка может занять много времени. Поставщики транспорта можно вызвать функцию обратного вызова [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для очереди MAPI часто во время такой обработки для освобождения времени использования Процессора для других системных задач. 
  
Всех получателей в таблице получателя, который создает поставщика транспорта для сообщение должно содержать все необходимые свойства адресации. В случае необходимости поставщика можно создать настраиваемые получателя для представления определенного получателя. Тем не менее если поставщик может осуществлять запись получателя, которая включает в себя дополнительные сведения, его следует сделать. Например если поставщика транспорта имеется достаточно сведений о формате получателя поставщика адресных книг, что может создать запись допустимый идентификатор получателя для этого формата, то построение идентификатор записи.
  
Если какие-либо свойства nontransmittable получены, поставщика транспорта не следует хранить их в новое сообщение. Тем не менее поставщика транспорта следует хранить все свойства передаваемого, она получает в новое сообщение.
  
Если входящее сообщение — отчетов о доставке или уведомление о недоставке и поставщика транспорта не может использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для создания отчета из исходного сообщения, поставщик должен самого заполнения сообщения с соответствующих свойств. Тем не менее поставщика транспорта не удается задать свойство сообщения **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Чтобы сохранить входящего сообщения в список соответствующего магазина сообщение MAPI после обработки, поставщика транспорта вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Если поставщик транспорта сообщения для передачи в очередь MAPI, его можно остановить входящего сообщения, возврат из вызова **StartMessage** без вызова **SaveChanges**.
  
Все объекты, поставщика транспорта открывает во время звонка **StartMessage** необходимо освободить перед возвращением. Тем не менее поставщик должен освобождает объект сообщения, диспетчер очереди MAPI изначально переданной в параметре _lpMessage_ . 
  
Если **StartMessage** возвращает ошибку, сообщения в процессе выпущен без необходимости изменения сохранены и теряется. В этом случае поставщика транспорта следует передать флаг NOTIFY_CRITICAL_ERROR с помощью вызова метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и вызовите метод [IXPLogon::Poll](ixplogon-poll.md) для уведомления диспетчер очереди MAPI, который находится в очень неблагоприятных ошибки. 
  
Для получения дополнительных сведений см [Диспетчер очереди MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

