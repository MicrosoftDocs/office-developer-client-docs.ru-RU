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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720410"
---
# <a name="users-collection-adox"></a>Коллекция Users (ADOX)

**Применимо к**: Access 2013, Office 2013

Содержит все хранимые объектов [пользователей](user-object-adox.md) из каталога или группы.

## <a name="remarks"></a>Замечания

Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей. Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.

Метод [Append](append-method-adox-users.md) для семейства сайтов **пользователей** является уникальным для ADOX. Вы можете выполнить указанные ниже действия.

- Добавление нового пользователя в коллекцию с помощью метода **Append** .

Остальные свойства и методы являются стандартными в семействах сайтов ADO. Вы можете выполнить указанные ниже действия.

- Права пользователя в коллекции с помощью свойства [элемента](item-property-ado.md) .

- Возвращает количество пользователей, содержащихся в коллекции со свойством [Count](count-property-ado.md) .

- Удаление пользователя из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

- Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.

> [!NOTE]
> Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.

