---
title: Поставщик транспорта и операционная модель MAPI Spooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426627"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Поставщик транспорта и операционная модель MAPI Spooler

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициализация, запуск, обработка, отключение и деинитиализация поставщика транспорта выполняются серией вызовов от пулера MAPI к поставщику транспорта. Вызовы последовательно следуют следующим образом:
  
1. Spooler MAPI вызывает [функцию XPProviderInit,](xpproviderinit.md) передает объект поддержки, получает объект поставщика и проверяет, что поставщик транспорта и spooler MAPI поддерживают совместимый диапазон номеров версий MAPI. 
    
2. Spooler MAPI вызывает [метод IXPProvider::TransportLogon](ixpprovider-transportlogon.md) [интерфейса IXPProvider: IUnknown.](ixpprovideriunknown.md) Сеанс устанавливается между пулером MAPI и поставщиком транспорта с учетными данными в текущем разделе профиля. Поставщик транспорта возвращает объект logon. 
    
3. Шпалер MAPI вызывает [метод IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Поставщик транспорта возвращает список уникальных идентификаторов (UID) и типов адресов электронной почты, которые он примет. 
    
4. Поставщик транспорта вызывает [метод IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для создания строки в таблице состояния MAPI. 
    
5. Spooler MAPI вызывает [метод IXPLogon::TransportNotify,](ixplogon-transportnotify.md) чтобы включить передачу и прием сообщений. 
    
6. Если поставщик транспорта запрашивает его в ответ на вызов **TransportLogon,** шпалер MAPI периодически вызывает [метод IXPLogon::Idle.](ixplogon-idle.md) Простая обработка полезна, если поставщику транспорта необходимо оповещение системы обмена сообщениями для новых сообщений или выполнение других задач с низким приоритетом. 
    
7. Spooler MAPI и поставщик транспорта отправляют и получают сообщения. Дополнительные сведения см. в [примере модели отправки сообщений и](message-submission-model.md) [модели приема сообщений.](message-reception-model.md) Пулер MAPI передает запросы и звонки на объекты поддержки, сообщения и вложения.
    
8. Spooler MAPI вызывает метод **TransportNotify,** чтобы отключить передачу и прием сообщений. 
    
9. Spooler MAPI выпускает объекты logon и provider. Дополнительные сведения см. в [методе IXPProvider::Shutdown.](ixpprovider-shutdown.md) 
    

