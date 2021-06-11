---
title: Необходимые функциональные возможности для поставщиков транспорта
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
# <a name="required-functionality-for-transport-providers"></a>Необходимые функциональные возможности для поставщиков транспорта

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Каждый поставщик транспорта MAPI должен:
  
- Следуйте общим рекомендациям по работе с MAPI и другими поставщиками услуг. Дополнительные сведения см. в [приложении MAPI Development](mapi-application-development.md) и [MAPI Service Providers.](mapi-service-providers.md)
    
- Чтобы поставщик транспорта DLL выставил MAPI функцию инициализации [XPProviderInit.](xpproviderinit.md) 
    
- Подвергайте MAPI реализации [интерфейсов IXPProvider : IUnknown](ixpprovideriunknown.md) и [IXPLogon: IUnknown.](ixplogoniunknown.md) 
    
- Подвергайте MAPI и клиентские приложения реализации [интерфейса IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Дополнительные сведения о реализации **IMAPIStatus** см. в дополнительных сведениях [о реализации объектов status.](status-object-implementation.md) 
    
- Реализация диалоговое окно листа свойств для настройки. Дополнительные сведения о реализации листов свойств см. в см. [в рубке Реализация листов свойств.](property-sheet-implementation.md)
    

