---
title: Коллекция пользователей (ADOX)
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
# <a name="users-collection-adox"></a>Коллекция пользователей (ADOX)

**Область применения**: Access 2013, Office 2013

Содержит все сохраненные [объекты](user-object-adox.md) пользователя каталога или группы.

## <a name="remarks"></a>Примечания

Коллекция **"Пользователи** [каталога"](catalog-object-adox.md) представляет всех пользователей каталога. Коллекция **Пользователей** для [группы представляет](group-object-adox.md) только пользователей, которые имеют членство в определенной группе.

Метод [Приложения](append-method-adox-users.md) для коллекции **Пользователей** уникален для ADOX. Вы получаете перечисленные ниже возможности.

- Добавьте нового пользователя в коллекцию с помощью метода **Append.**

Остальные свойства и методы являются стандартными для коллекций ADO. Вы получаете перечисленные ниже возможности.

- Доступ к пользователю в коллекции с [свойством Item.](item-property-ado.md)

- Возвращайте количество пользователей, содержащихся в коллекции, с помощью [свойства Count.](count-property-ado.md)

- Удалите пользователя из коллекции методом [Delete.](delete-method-adox-collections.md)

- Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью [метода Обновления.](refresh-method-ado.md)

> [!NOTE]
> Прежде чем примковать  объект Пользователя к коллекции  Пользователей объекта **Group,** объект User с тем же именем, что и объект, который должен быть придан, уже должен существовать в коллекции **Пользователей**  **каталога.** [](name-property-adox.md)

