---
title: Необходимые функции для поставщиков транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580497"
---
# <a name="required-functionality-for-transport-providers"></a>Необходимые функции для поставщиков транспорта

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Каждый поставщик транспорта MAPI выполнить следующие действия:
  
- Общие рекомендации по работе с MAPI и других поставщиков услуг. Для получения дополнительных сведений см [Разработки приложений MAPI](mapi-application-development.md) и [Поставщиков служб MAPI](mapi-service-providers.md).
    
- У поставщика транспорта DLL делает доступными для MAPI его функции инициализации [XPProviderInit](xpproviderinit.md) . 
    
- Предоставлять доступ MAPI его реализации [IXPProvider: IUnknown](ixpprovideriunknown.md) и [IXPLogon: IUnknown](ixplogoniunknown.md) интерфейсов. 
    
- Предоставлять доступ MAPI и клиентских приложениях его реализации [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса. Дополнительные сведения о реализации **IMAPIStatus**можно [Реализация объекта состояния](status-object-implementation.md). 
    
- Реализация диалогового окна Свойства таблицы конфигурации. Дополнительные сведения о реализации свойств можно [Реализация таблицы свойств](property-sheet-implementation.md).
    

