---
title: Отключение поставщика магазина сообщений
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
# <a name="shutting-down-a-message-store-provider"></a>Отключение поставщика магазина сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Если поставщик является поставщиком магазина сообщений, его можно закрыть одним из следующих способов:
  
- Когда клиент или шпалер MAPI вызывает [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). Отключение поставщика магазина сообщений с **помощью StoreLogoff** приводит к упорядочению и контролю остановки. 
    
- Когда клиент вызывает [IMAPISession::Logoff](imapisession-logoff.md). 
    
Реализация **IMsgStore::StoreLogoff** должна начинаться с вызова [IMAPISupport::StoreLogoffTransports,](imapisupport-storelogofftransports.md) чтобы сообщить MAPI о его закрытии, указав, что все связанные поставщики транспорта должны быть отключены. Когда **возвращается IMsgStore::StoreLogoff,** его вызыватель вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) магазина сообщений. Реализовать этот **метод выпуска,** назвав метод **IUnknown::Release** объекта поддержки. 
  
MAPI выполняет следующие задачи в реализации **IUnknown::Release** для магазинов сообщений: 
  
1. Удаляет все структуры [MAPIUID,](mapiuid.md) зарегистрированные поставщиком магазина сообщений. 
    
2. Удаляет строку поставщика хранения сообщений из таблицы состояния.
    
3. Вызывает [IMSLogon::Logoff,](imslogon-logoff.md) чтобы освободить все открытые объекты, подобекты и объекты состояния. 
    
4. Вызывает [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) чтобы освободить объект логотипа поставщика магазина сообщений. 
    
Некоторые клиенты могут отключить вызов **в IMsgStore::StoreLogoff,** инициав остановку поставщика магазина сообщений с помощью вызова метода **IUnknown::Release** магазина сообщений. При таких обстоятельствах отключение без вызова **в StoreLogoff** является менее упорядоченным и управляемым. Напишите метод выпуска  магазина сообщений для обработки этой возможности и отслеживайте, был ли звонок **в IMAPISupport::StoreLogoffTransports.** **StoreLogoffTransports** должен быть вызван один раз в процессе остановки. Если в методе **выпуска** обнаружено, что **StoreLogoffTransports** еще не вызывался, вызывайте его с LOGOFF_ABORT флагом. 
  
## <a name="see-also"></a>См. также



[Отключение поставщика услуг](shutting-down-a-service-provider.md)

