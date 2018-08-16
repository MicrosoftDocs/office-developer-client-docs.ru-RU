---
title: Иерархия вложенности MAPI объекта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 94fea23f71e6bc29b038db38f6f06cda0f85d635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809792"
---
# <a name="mapi-object-containment-hierarchy"></a>Иерархия вложенности MAPI объекта
  
**Относится к**: Outlook 
  
Отношения между объектами указывает зависимостей, некоторые объекты от других объектов для доступа. Для клиентского приложения доступ к объектам определенного разрешается доступ для других пользователей. В некоторых случаях отношения между объектами, реализованные поставщиком услуг за логической иерархии. В других случаях произвольных. 
  
Клиента необходимо получить доступ к объекту сеанса MAPI для использования многие другие объекты (например, для поставщиков услуг и адресной книги MAPI).
  
Включение хранилища сообщений основано на иерархическую связь между объектами в хранилище сообщений: хранилище сообщений объекта хранилища, папки, сообщения и вложения. Логически вложения, содержатся в сообщения, в папки и папки в хранилище сообщений. Отношения сопоставляет этой логической иерархии. Для получения доступа к сообщению, например, клиента необходимо сначала открыть папку, в которой содержится сообщение. Профили и объекты состояния приведены примеры более произвольных ограничивающую связь. Обе эти объекты доступны через сеанс. 
  
Некоторые объекты контейнеров обеспечить доступ. Вложения и получатели являются примерами объектов, которые полностью зависят от их контейнеров. Единственный способ доступа к вложения или получателя — по почте, к которой он принадлежит. Другие объекты имеют пути альтернативного доступа. Эти объекты назначаются двоичные идентификаторы, известных как идентификаторы записей поставщиками услуг, их создания. Идентификаторы записей можно использовать для доступа к своим объектам напрямую, включение клиентов для обхода дерева вложенности. 
  
На следующем рисунке показана иерархия вложенности MAPI. Сеанс находится в верхней части дерева, так как они через сеанс, что клиент получает доступ ко всем другим объектам. Следующий уровень включает в себя в таблице хранилища сообщений, объект таблицы, где перечислены свойства для всех поставщиков хранилища сообщений в текущем сеансе и адресной книги, чтобы предоставить доступ ко всем поставщиками адресной книги. Сообщение хранилища в таблице и адресной книги используются для доступа к объектам, реализуемый поставщиками определенной службы, далее в порядке вложенности.
  
**Иерархия вложений MAPI**
  
![Иерархия вложенности MAPI] (media/amapi_41.gif "Иерархия вложенности MAPI")
  
## <a name="see-also"></a>См. также

- [Обзор интерфейса и объект MAPI](mapi-object-and-interface-overview.md)
