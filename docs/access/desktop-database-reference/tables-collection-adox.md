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

Содержит все [объекты Table](table-object-adox.md) каталога.

## <a name="remarks"></a>Заметки

Метод [Append](append-method-adox-tables.md) для коллекции **Tables** уникален для ADOX. Вы можете выполнить указанные ниже действия.

  - Добавьте новую таблицу в коллекцию с помощью **метода Append.**

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

  - Доступ к таблице в коллекции с помощью [свойства Item.](item-property-ado.md)

  - Возвращает количество таблиц, содержащихся в коллекции, со свойством [Count.](count-property-ado.md)

  - Удалите таблицу из коллекции с помощью метода [Delete.](delete-method-adox-collections.md)

  - Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью метода [Refresh.](refresh-method-ado.md)

Некоторые поставщики могут возвращать другие объекты схемы, например View, в коллекции Tables. Поэтому некоторые коллекции ADOX могут содержать ссылки на один и тот же объект. Если удалить объект из одной коллекции, изменение не будет видно в другой коллекции, которая ссылается на удаленный объект, пока в коллекции не будет вызван метод Refresh. Например, при поставщике OLE DB для Microsoft Jet представления возвращаются вместе с коллекцией Tables. При сбросе представления необходимо обновить коллекцию Tables, прежде чем коллекция отразит изменение.

