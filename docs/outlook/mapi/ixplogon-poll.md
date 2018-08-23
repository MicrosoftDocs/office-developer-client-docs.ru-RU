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
ms.openlocfilehash: 3426854e727ebce7a2ac2243491994ce0e066ac6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591382"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, поставщика транспорта, полученных одного или нескольких входящих сообщений.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Параметры

 _lpulIncoming_
  
> [out] Значение, указывающее на наличие входящих сообщений. Ненулевое значение указывает на наличие входящих сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Диспетчер очереди MAPI, периодически вызывает метод **IXPLogon::Poll** , если поставщик транспорта указывает, что должно быть запрошено для новых сообщений, которые поставщик, передав LOGON_SP_POLL флаг, вызов [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) метод в начале сеанса. Если указывает поставщика транспорта в ответ на звонок **опроса** , что есть один или более входящего сообщения об ошибках для его к процессу, диспетчер очереди MAPI вызывает метод [IXPLogon::StartMessage](ixplogon-startmessage.md) , чтобы разрешить поставщика к процессу первый входящий трафик Сообщение. Поставщика транспорта указывает входящих сообщений, указав значение с помощью параметра _lpulIncoming_ ненулевое значение. 
  
## <a name="see-also"></a>См. также



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

