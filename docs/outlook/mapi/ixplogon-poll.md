---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425276"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, получил ли поставщик транспорта одно или несколько входящие сообщения.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Parameters

 _lpulIncoming_
  
> [вышел] Значение, которое указывает на наличие входящие сообщения. Значение nonzero указывает на входящие сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Шпалер MAPI периодически вызывает метод **IXPLogon::P oll,** если поставщик транспорта указывает, что он должен быть оповещен о новых сообщениях, которые поставщик делает, передав флаг LOGON_SP_POLL вызову [методу IXPProvider::TransportLogon](ixpprovider-transportlogon.md) в начале сеанса. Если поставщик транспорта указывает в ответ на вызов **Poll,** что для обработки доступно одно или несколько входящие сообщения, пуллер MAPI вызывает [метод IXPLogon::StartMessage,](ixplogon-startmessage.md) чтобы разрешить поставщику обрабатывать первое входящий сообщение. Поставщик транспорта указывает входящие сообщения, установив значение параметра  _lpulIncoming_ к значению nonzero. 
  
## <a name="see-also"></a>См. также



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

