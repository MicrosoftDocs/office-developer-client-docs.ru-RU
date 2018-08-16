---
title: Объекты, реализуемые MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fe5549e41008dbf5b5f50f9f32769f1a820e3bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809763"
---
# <a name="mapi-implemented-objects"></a>Объекты, реализуемые MAPI
  
**Относится к**: Outlook 
  
Несколько объектов для использования клиентскими приложениями и поставщиками услуг, реализуемые программным интерфейсом MAPI. Объект сеанса позволяет клиентам использовать сеанса служб для доступа к таблицам, а также для связи с поставщиками услуг. Объект адресной книги предоставляет клиентам для интегрированной доступ ко всем поставщиками различных адресной книги. 
  
MAPI предоставляет несколько объектов в таблице и состояние для клиентов использовать для просмотра и мониторинг сеанса и службы сведения о поставщике. Например MAPI предоставляет таблица профиля с сведения о всех профилей, установленных на компьютере и таблица службы сообщений с сведения обо всех служб сообщение в текущий профиль. MAPI предоставляет три различных состояния объектов: одно, который представляет общий подсистемы, одно для очереди MAPI и для интегрированной адресной книги. 
  
Четыре разных объектов для управления конфигурацией службы сообщений, поставщиков услуг и профилей, реализуемые программным интерфейсом MAPI. Клиенты и поставщики услуг используйте администрирования поставщика и объекты раздела профиля; Эти объекты включить их для настройки поставщиков услуг и доступа к свойствам профилей. Клиенты используют только службы сообщений и объекты администрирования профиля, объекты, которые поддерживают администрирования службы сообщений и профилей. 
  
MAPI предоставляет два объекта для поставщиков услуг: поддержка объектов и TNEF. Все поставщики услуг использовать один или несколько объектов поддержки; Существует четыре реализации поддержки различных объектов. MAPI предоставляет реализацию для поддержки конфигурации, а также определенных реализаций для поддержки адресной книги, хранилища сообщений и поставщиками транспорта. Объект TNEF используется поставщиками транспорта, которые поддерживают транспорта Neutral Encapsulation формата TNEF.
  
Два объекта служебной программы, в таблице данных и данных свойства, обычно используется поставщиками услуг. Объекты данных в таблице помощи в реализации объектов в таблице; Справка объекты данных свойства для доступа к свойству set и представления и помощь в реализации [IMAPIProp: IUnknown](imapipropiunknown.md), интерфейс базового свойства. 
  
В следующей таблице обобщаются назначения для каждого объекта, который реализует MAPI.
  
|**Объект MAPI**|**Описание**|
|:-----|:-----|
|Адресная книга  <br/> |Предоставляет доступ к интегрированное представление сведений для получателя, которому принадлежит со всеми поставщиками адресной книги в текущей конфигурации.  <br/> |
|Администрирование службы сообщений  <br/> |Предоставляет доступ к сведения о службе сообщений для конфигурации.  <br/> |
|Администрирование профилей  <br/> |Предоставляет доступ к информации профилей для конфигурации.  <br/> |
|Раздел профиля  <br/> |Часть профиля, используемого для описания службы конкретное сообщение или поставщика услуг.  <br/> |
|Свойство данных  <br/> |Поддерживает доступ к свойствам и приводятся рекомендации по реализации **IMAPIProp**.  <br/> |
|Администрирование поставщика  <br/> |Предоставляет доступ к сведения о поставщике услуг для конфигурации.  <br/> |
|Сеанс  <br/> |Представляет подключение к базовым систем обмена сообщениями и предоставляет клиентам доступ к ресурсам MAPI.  <br/> |
|Status  <br/> |Предоставляет доступ к состоянию подсистемы MAPI, адресной книги или диспетчер очереди MAPI.  <br/> |
|Поддержка  <br/> |Эта статья поможет поставщиков услуг обработки запросов клиентов.  <br/> |
|Таблица  <br/> |Предоставляет доступ к сводное представление данных объекта в формате строк и столбцов, аналогичную таблицы базы данных.  <br/> |
|Таблицы данных  <br/> |Поддерживает доступ к данным таблицы и реализует объекты в таблице.  <br/> |
|ФОРМАТ TNEF  <br/> |Поддерживает использование из транспорта Neutral Encapsulation формата TNEF.  <br/> |
   
На следующем рисунке показана связь между объекты, внедряемые MAPI, интерфейсы, с которых они наследуют и компоненты, которые их использования. 
  
**Объекты, внедряемые MAPI**
  
![Объекты, внедряемые MAPI] (media/amapi_68.gif "Объекты, внедряемые MAPI")
  
## <a name="see-also"></a>См. также

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Обзор интерфейса и объект MAPI](mapi-object-and-interface-overview.md)
