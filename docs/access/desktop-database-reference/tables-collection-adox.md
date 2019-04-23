---
title: Коллекция Tables (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314051"
---
# <a name="tables-collection-adox"></a>Коллекция Tables (ADOX)


**Область применения**: Access 2013, Office 2013

Содержит все объекты [Table](table-object-adox.md) каталога.

## <a name="remarks"></a>Примечания

Метод [append](append-method-adox-tables.md) для коллекции **Tables** является уникальным для ADOX. Вы можете выполнить указанные ниже действия.

  - Добавление новой таблицы в коллекцию с помощью метода **append** .

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

  - Доступ к таблице в коллекции со свойством [Item](item-property-ado.md) .

  - Возвращает количество таблиц, хранящихся в коллекции, со свойством [Count](count-property-ado.md) .

  - Удаление таблицы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

  - Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .

Некоторые поставщики могут возвращать другие объекты схемы, например представление, в коллекции Tables. Таким образом, некоторые коллекции ADOX могут содержать ссылки на один и тот же объект. Если вы удалите объект из одной коллекции, это изменение не будет отображаться в другой коллекции, ссылающейся на удаленный объект, пока не будет вызван метод Refresh в коллекции. Например, при использовании поставщика OLE DB для Microsoft Jet представления возвращаются с помощью коллекции Tables. При удалении представления необходимо обновить коллекцию Tables, прежде чем коллекция будет отражать изменение.

