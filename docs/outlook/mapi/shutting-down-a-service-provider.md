---
title: Отключение поставщика услуг
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339209"
---
# <a name="shutting-down-a-service-provider"></a>Отключение поставщика услуг

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Когда клиент вызывает [метод IMAPISession::Logoff,](imapisession-logoff.md) чтобы закончить сеанс и закрыть все активные поставщики услуг, MAPI в свою очередь вызывает следующие методы: 
  
- [IABLogon::Logoff](iablogon-logoff.md) для поставщиков адресных книг. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) для поставщиков магазинов сообщений. 
    
- [IXPLogon::TransportLogoff для](ixplogon-transportlogoff.md) поставщиков транспорта. 
    
Эти методы имеют аналогичные реализации. Основные задачи, выполняемые методом журнала:
  
- Освобождение всех открытых объектов, включая подобекты и объекты состояния.
    
- Вызов метода [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта поддержки для усугубления его отсчета ссылок. 
    
- Удаление всех зарегистрированных структур [MAPIUID](mapiuid.md) поставщика. 
    
- Удаление строки поставщика в таблице состояния.
    
- Выполнение любых задач, которые связаны с очисткой ресурсов, например следующие:
    
  - Прекращение подключения к удаленному серверу.
    
  - Decrementing the reference count on the logon object.
    
  - Удаление объекта logon из списка объектов logon, которые хранит поставщик.
    
  - В режиме отлаживания выдают следы, чтобы найти объекты с утечкой памяти.
    
Когда метод входа возвращается, MAPI вызывает следующее:
  
- Метод **IUnknown::Release** объекта вашего логона. 
    
- Метод отключения объекта поставщика **для** выполнения любых задач окончательной очистки. В зависимости от типа поставщика один из следующих методов называется: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) для поставщиков адресных книг 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) для поставщиков магазинов сообщений 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) для поставщиков транспорта 
    
- Метод **IUnknown::Release** объекта поставщика. 
    
Если поставщик является хранилищем сообщений, клиентский вызов [в IMsgStore::StoreLogoff](imsgstore-storelogoff.md) также инициирует процесс остановки. **StoreLogoff** закрывает одного конкретного поставщика магазина сообщений и не влияет на сеанс. Только поставщик магазина сообщений может быть закрыт с помощью этого метода; нет явного способа отключения конкретной адресной книги или поставщика транспорта. Сведения о том, как реагировать на вызов **StoreLogoff,** см. в сообщении [Shutting Down a Message Store Provider.](shutting-down-a-message-store-provider.md)
  
DLL поставщика будет выгружена, когда MAPI вызывает функцию API **Win32 FreeLibrary**, вызов, который сделан после того, как последний активный клиент вызывает [MAPIUninitialize](mapiuninitialize.md). К этому времени поставщик услуг завершит работу. 
  
## <a name="see-also"></a>См. также



[Поставщики услуг MAPI](mapi-service-providers.md)

