---
title: Завершение работы поставщика store сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339202"
---
# <a name="shutting-down-a-message-store-provider"></a>Завершение работы поставщика store сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если ваш поставщик является поставщиком store сообщений, его можно отключить одним из следующих способов:
  
- Когда клиент или пулер MAPI вызывает [IMsgStore::StoreLogoff.](imsgstore-storelogoff.md) Отключение поставщика хранения сообщений с **помощью StoreLogoff** приводит к упорядочению и контролю завершения работы. 
    
- Когда клиент вызывает [IMAPISession::Logoff.](imapisession-logoff.md) 
    
Реализация **IMsgStore::StoreLogoff** должна начинаться с вызова [IMAPISupport::StoreLogoffTransports,](imapisupport-storelogofftransports.md) чтобы сообщить MAPI о том, что она закрывается, указывая, что все связанные поставщики транспорта должны быть отключены. Когда **возвращается IMsgStore::StoreLogoff,** его вызыватель вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) вашего магазина сообщений. Реализуя **этот метод Release,** вы вызываете метод **IUnknown::Release** объекта поддержки. 
  
MAPI выполняет следующие задачи в реализации **IUnknown::Release** для хранилищ сообщений: 
  
1. Удаляет все структуры [MAPIUID,](mapiuid.md) зарегистрированные поставщиком store сообщений. 
    
2. Удаляет строку поставщика хранения сообщений из таблицы состояния.
    
3. Вызывает [IMSLogon::Logoff,](imslogon-logoff.md) чтобы освободить все открытые объекты, подобекты и объекты состояния. 
    
4. Вызывает [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) чтобы освободить объект для логотипа поставщика store сообщений. 
    
Некоторые клиенты могут опустить вызов **IMsgStore::StoreLogoff,** инициав завершение работы поставщика вашего магазина сообщений с помощью вызова метода **IUnknown::Release** в хранилище сообщений. При таких обстоятельствах завершение работы без вызова **StoreLogoff** является менее упорядоченным и контролируемым. Запишите метод release  вашего магазина сообщений, чтобы обработать эту возможность и отслеживать, произошел ли вызов **IMAPISupport::StoreLogoffTransports.** Во время завершения работы необходимо один раз вызвано хранилище **StoreLogoffTransports.** Если вы обнаружите в методе **Release,** что **StoreLogoffTransports** еще не был вызван, вы можете вызвать его с LOGOFF_ABORT флагом. 
  
## <a name="see-also"></a>См. также



[Завершение работы поставщика услуг](shutting-down-a-service-provider.md)

