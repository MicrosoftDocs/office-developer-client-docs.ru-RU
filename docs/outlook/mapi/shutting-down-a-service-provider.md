---
title: Завершение работы поставщика услуг
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
# <a name="shutting-down-a-service-provider"></a>Завершение работы поставщика услуг

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md) для окончания сеанса и отключения всех активных поставщиков услуг, MAPI, в свою очередь, вызывает следующие методы: 
  
- [IABLogon::Logoff](iablogon-logoff.md) для поставщиков адресных книг. 
    
- [IMSLogon::Logoff](imslogon-logoff.md) для поставщиков store сообщений. 
    
- [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) для поставщиков транспорта. 
    
Эти методы имеют похожие реализации. Основные задачи, выполняемые методом logoff:
  
- Освобождение всех открытых объектов, включая подобекты и объекты состояния.
    
- Вызов метода [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта поддержки для укрупления его опорного подсчета. 
    
- Удаление всех зарегистрированных структур [MAPIUID](mapiuid.md) поставщика. 
    
- Удаление строки поставщика в таблице состояния.
    
- Выполнение любых задач, которые связаны с очисткой ресурсов, например:
    
  - Прерывание подключения к удаленному серверу.
    
  - Decrementing the reference count on the logon object.
    
  - Удаление объекта для логотипа из списка объектов для логотипа, которые хранит поставщик.
    
  - В режиме отлаживания выдают трассировки для поиска объектов, которые имеют утечку памяти.
    
Когда метод logoff возвращается, MAPI вызывает следующие вызовы:
  
- Метод **IUnknown::Release** объекта для вашего logon. 
    
- Метод Завершения работы объекта **поставщика для** выполнения любых окончательных задач очистки. В зависимости от типа поставщика, будет вызван один из следующих методов: 
    
  - [IABProvider::Shutdown](iabprovider-shutdown.md) для поставщиков адресных книг 
    
  - [IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers 
    
  - [IXPProvider::Shutdown](ixpprovider-shutdown.md) для поставщиков транспорта 
    
- Метод **IUnknown::Release** объекта поставщика. 
    
Если ваш поставщик является хранилищем сообщений, клиентский вызов [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) также инициирует процесс завершения работы. **StoreLogoff** закрывает одного конкретного поставщика store сообщений и не влияет на сеанс. С помощью этого метода можно отключить только поставщика store сообщений; явного способа отключения определенной адресной книги или поставщика транспорта не существует. Сведения о том, как реагировать на вызов **StoreLogoff,** см. в сообщении [Shutting Down a Message Store Provider.](shutting-down-a-message-store-provider.md)
  
DLL поставщика будет выгружена, когда MAPI вызывает функцию Win32 API **FreeLibrary**, вызов, который сделан после того, как последний активный клиент вызвал [MAPIUninitialize](mapiuninitialize.md). К этому времени поставщик услуг завершит работу. 
  
## <a name="see-also"></a>См. также



[Поставщики услуг MAPI](mapi-service-providers.md)

