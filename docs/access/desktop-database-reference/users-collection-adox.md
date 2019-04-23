---
title: Коллекция Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312938"
---
# <a name="users-collection-adox"></a>Коллекция Users (ADOX)

**Область применения**: Access 2013, Office 2013

Содержит все сохраненные объекты [пользователя](user-object-adox.md) для каталога или группы.

## <a name="remarks"></a>Примечания

Коллекция **Users** [каталога](catalog-object-adox.md) Users содержит все пользователи каталога. Коллекция **Users** для [группы](group-object-adox.md) представляет только тех пользователей, у которых есть членство в определенной группе.

Метод [append](append-method-adox-users.md) для коллекции **Users** уникален для ADOX. Вы можете выполнить указанные ниже действия.

- Добавьте нового пользователя в коллекцию с помощью метода **append** .

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

- Доступ к пользователю в коллекции со свойством [Item](item-property-ado.md) .

- Возврат числа пользователей, включенных в коллекцию, со свойством [Count](count-property-ado.md) .

- Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

- Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .

> [!NOTE]
> Перед добавлением объекта **User** в коллекцию **Users** объекта **Group** объект **пользователя** с тем же [именем](name-property-adox.md) , что и у добавляемОго объекта, должен уже существовать в коллекции Users **каталога**. ****

