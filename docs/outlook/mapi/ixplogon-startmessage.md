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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициирует передачу входящие сообщения от поставщика транспорта в пулер MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpMessage_
  
> [in] Указатель на объект сообщения (представляющий входящий сигнал), который имеет разрешение на чтение и записи, который используется поставщиком транспорта для доступа к этому сообщению и управления им. Этот объект остается действительным до тех пор, пока поставщик транспорта не вернется из вызова **в IXPLogon::StartMessage.**
    
 _lpulMsgRef_
  
> [вышел] Указатель на ссылку, назначенную сообщению. Spooler MAPI инициализирует это значение до 1, прежде чем он возвращает указатель поставщику транспорта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает **метод IXPLogon::StartMessage,** чтобы инициировать передачу входящие сообщения от поставщика транспорта в spooler MAPI. Прежде чем поставщик транспорта начнет использовать сообщение, на которое указывает _lpMessage,_ он должен хранить ссылку на сообщение в параметре _lpulMsgRef_ для потенциального использования вызовом метода [IXPLogon::TransportNotify.](ixplogon-transportnotify.md) 
  
Во время **вызова StartMessage** пулер MAPI обрабатывает методы для объектов, открытых во время передачи сообщения, а также обрабатывает любые вложения. Эта обработка может занять много времени. Поставщики транспорта могут часто вызывать [функцию вызова IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для пулера MAPI во время этой обработки, чтобы освободить время ЦП для других системных задач. 
  
Все получатели в таблице получателей, которую создает поставщик транспорта для сообщения, должны содержать все необходимые свойства адресов. При необходимости поставщик может создать настраиваемый получатель для представления конкретного получателя. Однако если поставщик может создать запись получателя, которая включает дополнительные сведения, он должен это сделать. Например, если поставщик транспорта обладает достаточным количеством сведений о формате получателя поставщика адресной книги, что он может создать допустимый идентификатор входа для получателя для этого формата, он должен создать идентификатор записи.
  
Если получены какие-либо нетрансмитируемые свойства, поставщик транспорта не должен хранить их в новом сообщении. Однако поставщик транспорта должен хранить все передаваемые свойства, которые он получает в новом сообщении.
  
Если входящие сообщения — это отчет о доставке или отчет о неделивстве, а поставщик транспорта не может использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для создания отчета из исходного сообщения, поставщик должен сам заполнить сообщение соответствующими свойствами. Однако поставщик транспорта не может установить  свойство PR_ENTRYID[(PidTagEntryId).](pidtagentryid-canonical-property.md)
  
Чтобы сохранить входящие сообщения в соответствующем хранилище сообщений MAPI после обработки, поставщик транспорта вызывает [метод IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Если у поставщика транспорта нет сообщений, которые можно передать в пульпер MAPI, он может остановить входящий сигнал, возвращаясь с вызова **StartMessage** без вызова **SaveChanges.**
  
Все объекты, открываемые поставщиком транспорта во время вызова **StartMessage,** должны быть освобождены перед возвращением. Однако поставщик не должен выпускать объект сообщения, который был изначально передан пулером MAPI в _параметре lpMessage._ 
  
Если **StartMessage** возвращает ошибку, сообщение в процессе выпускается без сэкономленных изменений и теряется. В этом случае поставщик транспорта должен передать флаг NOTIFY_CRITICAL_ERROR с вызовом в метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и вызвать [метод IXPLogon::P oll,](ixplogon-poll.md) чтобы уведомить шпалер MAPI о том, что он находится в состоянии серьезной ошибки. 
  
Дополнительные сведения см. [в см. в ссылке Interacting with the MAPI Spooler.](interacting-with-the-mapi-spooler.md) 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

