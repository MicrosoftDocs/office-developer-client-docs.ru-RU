---
title: Завершение работы поставщика хранилища сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386056"
---
# <a name="shutting-down-a-message-store-provider"></a>Завершение работы поставщика хранилища сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если ваш поставщик поставщика хранилища сообщений, его можно завершить работу в одном из следующих способов:
  
- Если это клиент или диспетчер очереди MAPI вызывает [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). Завершение работы поставщика хранилища сообщений с **StoreLogoff** вызывает завершение работы в надлежащей и управляемым процессом. 
    
- Когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md). 
    
Реализация **IMsgStore::StoreLogoff** должен начинаться с вызова [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) для оповещения MAPI, что оно завершает работу, указывающее регистрацию поставщиков, связанных с ними транспорта. При возврате **IMsgStore::StoreLogoff** , вызывающий вызывает метод [функции IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) хранилища сообщений. Реализуйте метод в этом **выпуске** , вызвав метод **функции IUnknown::Release** объекта поддержки. 
  
При реализации **функции IUnknown::Release** для хранилищ сообщений MAPI выполняет следующие задачи: 
  
1. Удаляет все структуры [MAPIUID](mapiuid.md) , зарегистрированные поставщиком хранилища сообщений. 
    
2. Удаляет поставщика хранилища сообщений строку из таблицы состояния.
    
3. Вызывает [IMSLogon::Logoff](imslogon-logoff.md) для освобождения всех открытых объектов, вложенных объектов и объектов состояние. 
    
4. Вызывает [функции IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) для освобождения объект поставщика хранилища сообщений входа в систему. 
    
Некоторые клиенты могут пропустить вызов **IMsgStore::StoreLogoff**, инициализация завершения конкретного поставщика хранилища сообщений с помощью вызова метода **функции IUnknown::Release** хранилища сообщений. Завершение работы при следующих условиях без вызова **StoreLogoff** менее нормального и управляемой. Метод **выпуске** хранилища сообщений для обработки этой возможности и отслеживание ли вызов **IMAPISupport::StoreLogoffTransports** произошла Write. **StoreLogoffTransports** необходимо вызывать один раз при завершении работы. Если в методе **выпуске** определяет, что **StoreLogoffTransports** еще не был вызван, вызовите с флагом LOGOFF_ABORT. 
  
## <a name="see-also"></a>См. также



[Завершение работы поставщика службы](shutting-down-a-service-provider.md)

