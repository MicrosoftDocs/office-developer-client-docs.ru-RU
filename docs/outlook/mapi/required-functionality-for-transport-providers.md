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
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404444"
---
# <a name="required-functionality-for-transport-providers"></a>Необходимые функции для поставщиков транспорта

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Каждый поставщик транспорта MAPI должен:
  
- Следуйте общим рекомендациям по работе с MAPI и другими поставщиками услуг. Дополнительные сведения см. в сведениях о [разработке приложений MAPI](mapi-application-development.md) и [поставщиках услуг MAPI.](mapi-service-providers.md)
    
- DLL поставщика транспорта предоставляет MAPI функцию инициализации [XPProviderInit.](xpproviderinit.md) 
    
- Доступ к MAPI его реализации [IXPProvider : IUnknown](ixpprovideriunknown.md) и [IXPLogon : интерфейсы IUnknown.](ixplogoniunknown.md) 
    
- Доступ к интерфейсу MAPI и клиентских приложений с реализацией [интерфейса IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Дополнительные сведения о реализации **IMAPIStatus** см. в реализации [объекта status.](status-object-implementation.md) 
    
- Реализуйте диалоговое окно таблицы свойств для настройки. Дополнительные сведения о реализации листов свойств см. в [реализации листа свойств.](property-sheet-implementation.md)
    

