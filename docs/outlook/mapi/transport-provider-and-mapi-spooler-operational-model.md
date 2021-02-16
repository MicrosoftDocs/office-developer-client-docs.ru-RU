---
title: Операционная модель поставщика транспорта и пула MAPI
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
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Операционная модель поставщика транспорта и пула MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициализация, запуск, обработка, завершение и деинициализация поставщика транспорта выполняются с помощью серии вызовов из пула MAPI к поставщику транспорта. Вызовы в порядке последовательности:
  
1. Пулер MAPI вызывает функцию [XPProviderInit,](xpproviderinit.md) передает объект поддержки, получает объект поставщика и проверяет, поддерживает ли поставщик транспорта и пулер MAPI совместимый диапазон номеров версий MAPI. 
    
2. Пулер MAPI вызывает метод [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) [интерфейса IXPProvider : IUnknown.](ixpprovideriunknown.md) Сеанс устанавливается между пулером MAPI и поставщиком транспорта с учетными данными в текущем разделе профиля. Поставщик транспорта возвращает объект для логотипа. 
    
3. Пулер MAPI вызывает метод [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Поставщик транспорта возвращает список уникальных идентификаторов (UID) и типов адресов электронной почты, которые он будет принимать. 
    
4. Поставщик транспорта вызывает метод [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы создать свою строку в таблице состояния MAPI. 
    
5. Пулер MAPI вызывает метод [IXPLogon::TransportNotify,](ixplogon-transportnotify.md) чтобы включить передачу и прием сообщений. 
    
6. Если поставщик транспорта запрашивает его в ответ на вызов **TransportLogon,** пулер MAPI периодически вызывает метод [IXPLogon::Idle.](ixplogon-idle.md) Обработка без простоя полезна, если поставщику транспорта необходимо оповещение системы обмена сообщениями на новые сообщения или выполнение других задач с низким приоритетом. 
    
7. Поставщик услуг пула MAPI и поставщик транспорта отправляют и получают сообщения. Дополнительные сведения см. в [модели отправки сообщений](message-submission-model.md) и [модели приема сообщений.](message-reception-model.md) MapI spooler services transport requests and calls on support, message, and attachment objects.
    
8. Пулер MAPI вызывает метод **TransportNotify,** чтобы отключить передачу и прием сообщений. 
    
9. Пульер MAPI освобождает объекты для выхода и поставщиков. Дополнительные сведения см. в [методе IXPProvider::Shutdown.](ixpprovider-shutdown.md) 
    

