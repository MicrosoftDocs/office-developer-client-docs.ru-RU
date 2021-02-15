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

Содержит все [хранимые](user-object-adox.md) объекты пользователя каталога или группы.

## <a name="remarks"></a>Заметки

Коллекция **"Пользователи"** [каталога](catalog-object-adox.md) представляет всех пользователей каталога. Коллекция **Users** для [группы представляет](group-object-adox.md) только пользователей, которые являются членами определенной группы.

Метод [Append](append-method-adox-users.md) для коллекции **Users** уникален для ADOX. Вы можете выполнить указанные ниже действия.

- Добавьте нового пользователя в коллекцию с помощью метода **Append.**

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

- Доступ к пользователю в коллекции с помощью [свойства Item.](item-property-ado.md)

- Возвращает количество пользователей, содержащихся в коллекции, со свойством [Count.](count-property-ado.md)

- Удаление пользователя из коллекции с помощью метода [Delete.](delete-method-adox-collections.md)

- Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью метода [Refresh.](refresh-method-ado.md)

> [!NOTE]
> Прежде чем приместь объект [](name-property-adox.md) **User** к коллекции **Users** объекта **Group,** объект **User** с тем же именем, что и объект, который необходимо к ним примедить, должен уже существовать в коллекции **Users** **каталога.**

