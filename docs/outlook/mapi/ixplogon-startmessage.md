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
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427607"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициирует передачу входящие сообщения от поставщика транспорта в пулер MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpMessage_
  
> [in] Указатель на объект сообщения (представляющий входящие сообщения), который имеет разрешение на чтение и записи, которое используется поставщиком транспорта для доступа к этому сообщению и управления им. Этот объект остается действительным до тех пор, пока поставщик транспорта не вернется из вызова **IXPLogon::StartMessage.**
    
 _lpulMsgRef_
  
> [out] Указатель на значение ссылки, назначенное сообщению. Пулер MAPI инициализирует это значение до 1, прежде чем возвращает указатель поставщику транспорта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::StartMessage,** чтобы инициировать передачу входящие сообщения от поставщика транспорта в пулер MAPI. Прежде чем поставщик транспорта начнет использовать сообщение, на которое указывает _lpMessage,_ он должен сохранить ссылку на сообщение в параметре _lpulMsgRef_ для возможного использования вызовом метода [IXPLogon::TransportNotify.](ixplogon-transportnotify.md) 
  
Во время **вызова StartMessage** пулер MAPI обрабатывает методы для объектов, открытых во время передачи сообщения, а также обрабатывает любые вложения. Эта обработка может занять много времени. Поставщики транспорта могут часто вызывать функцию вызова [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для пула MAPI во время этой обработки, чтобы освободить время ЦП для других системных задач. 
  
Все получатели в таблице получателей, которую поставщик транспорта создает для сообщения, должны содержать все необходимые свойства адресов. При необходимости поставщик может создать настраиваемую получатель для представления определенного получателя. Однако если поставщик может создать запись получателя, которая содержит дополнительные сведения, он должен сделать это. Например, если у поставщика транспорта достаточно сведений о формате получателя для поставщика адресной книги, он может создать допустимый идентификатор записи для получателя для этого формата, он должен создать идентификатор записи.
  
Если получены какие-либо неиспроверяемые свойства, поставщик транспорта не должен хранить их в новом сообщении. Однако поставщик транспорта должен хранить все передаваемые свойства, получаемые в новом сообщении.
  
Если входящие сообщения являются отчетом о доставке или ненастоячивым отчетом, а поставщик транспорта не может использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для создания отчета из исходного сообщения, поставщик должен самостоятельно заполнить сообщение соответствующими свойствами. Однако поставщик транспорта не может установить свойство PR_ENTRYID **(** [PidTagEntryId).](pidtagentryid-canonical-property.md)
  
Чтобы сохранить входящие сообщения в соответствующем хранилище сообщений MAPI после обработки, поставщик транспорта вызывает метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Если у поставщика транспорта нет сообщений, которые необходимо передать в пул MAPI, он может остановить входящие сообщения, вернувшись из вызова **StartMessage** без вызова **SaveChanges.**
  
Все объекты, которые поставщик транспорта открывает во время вызова **StartMessage,** должны быть освобождены перед возвратом. Однако поставщик не должен освободить объект сообщения, который пул MAPI изначально передал в _параметре lpMessage._ 
  
Если **StartMessage** возвращает ошибку, то сообщение, которое обрабатывается, будет освобождено без с сохраненных изменений и потеряно. В этом случае поставщик транспорта должен передать флаг NOTIFY_CRITICAL_ERROR с вызовом метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и вызвать метод [IXPLogon::P oll,](ixplogon-poll.md) чтобы уведомить пульер MAPI о серьезной ошибке. 
  
Дополнительные сведения [см. в сведениях о взаимодействии с пулером MAPI.](interacting-with-the-mapi-spooler.md) 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

