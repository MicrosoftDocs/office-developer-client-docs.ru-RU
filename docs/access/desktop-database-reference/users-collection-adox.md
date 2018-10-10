---
title: Users Collection (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d68dc2dd368523e8ca3dd04a06008cea9bef337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480233"
---
# <a name="users-collection-adox"></a>Users Collection (ADOX)


**Применимо к**: Access 2013 | Office 2013

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
> <P>Перед добавлением объекта <STRONG>пользователя</STRONG> в коллекцию <STRONG>пользователей</STRONG> объекта <STRONG>группы</STRONG> , объект <STRONG>пользователя</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекции <STRONG>пользователей</STRONG> из <STRONG>каталога</STRONG>.</P>


