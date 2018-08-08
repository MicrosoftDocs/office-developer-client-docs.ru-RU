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
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809632"
---
# <a name="ixplogonpoll"></a>IXPLogon::Poll

  
  
**Относится к**: Outlook 
  
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

