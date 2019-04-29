---
title: Иксплогонполл
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, получил ли поставщик транспорта одно или несколько входящих сообщений.
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a>Параметры

 _Лпулинкоминг_
  
> вышли Значение, указывающее на наличие входящих сообщений. Ненулевое значение указывает на наличие входящих сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI периодически вызывает метод **иксплогон::P олл** , если поставщик транспорта указывает, что он должен опрашиваться на наличие новых сообщений, которые поставщик выполняет, ПЕРЕДАВ флаг логон_сп_полл в вызов [Иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) в начале сеанса. Если поставщик транспорта указывает в ответ на вызов **опроса** , для обработки которого доступно одно или несколько входящих сообщений, то диспетчер очереди MAPI вызывает метод [Иксплогон:: стартмессаже](ixplogon-startmessage.md) , который позволяет поставщику обработать первый входящий Сообщение. Поставщик транспорта указывает на входящие сообщения, присвоив параметру _лпулинкоминг_ значение ненулевого значения. 
  
## <a name="see-also"></a>См. также



[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

