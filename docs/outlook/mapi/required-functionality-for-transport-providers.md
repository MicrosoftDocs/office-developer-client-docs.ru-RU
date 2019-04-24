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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328688"
---
# <a name="required-functionality-for-transport-providers"></a>Необходимые функции для поставщиков транспорта

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Каждый поставщик транспорта MAPI должен:
  
- Следуйте общим рекомендациям по работе с MAPI и другим поставщикам услуг. Дополнительные сведения можно найти в разделе [Разработка приложений MAPI](mapi-application-development.md) и [поставщики службы MAPI](mapi-service-providers.md).
    
- Библиотека DLL поставщика транспорта предоставляет MAPI функцию инициализации [ксппровидеринит](xpproviderinit.md) для MAPI. 
    
- Предоставьте интерфейсу MAPI реализацию интерфейсов [иксппровидер: IUnknown](ixpprovideriunknown.md) и [иксплогон: IUnknown](ixplogoniunknown.md) . 
    
- Предоставление приложениям MAPI и клиентским приложениям своей реализации интерфейса [имапистатус: IMAPIProp](imapistatusimapiprop.md) . Более подробную информацию о реализации **имапистатус**можно узнать в разделе [Status Object реализация](status-object-implementation.md). 
    
- Реализация диалогового окна "страница свойств" для конфигурации. Дополнительные сведения о реализации страниц свойств можно найти в статье [Реализация листа свойств](property-sheet-implementation.md).
    

