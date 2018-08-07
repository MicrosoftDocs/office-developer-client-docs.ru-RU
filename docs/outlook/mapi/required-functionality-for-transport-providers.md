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
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812150"
---
# <a name="required-functionality-for-transport-providers"></a>Необходимые функции для поставщиков транспорта

  
  
**Относится к**: Outlook 
  
Каждый поставщик транспорта MAPI выполнить следующие действия:
  
- Общие рекомендации по работе с MAPI и других поставщиков услуг. Для получения дополнительных сведений см [Разработки приложений MAPI](mapi-application-development.md) и [Поставщиков служб MAPI](mapi-service-providers.md).
    
- У поставщика транспорта DLL делает доступными для MAPI его функции инициализации [XPProviderInit](xpproviderinit.md) . 
    
- Предоставлять доступ MAPI его реализации [IXPProvider: IUnknown](ixpprovideriunknown.md) и [IXPLogon: IUnknown](ixplogoniunknown.md) интерфейсов. 
    
- Предоставлять доступ MAPI и клиентских приложениях его реализации [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса. Дополнительные сведения о реализации **IMAPIStatus**можно [Реализация объекта состояния](status-object-implementation.md). 
    
- Реализация диалогового окна Свойства таблицы конфигурации. Дополнительные сведения о реализации свойств можно [Реализация таблицы свойств](property-sheet-implementation.md).
    

