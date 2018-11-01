---
title: Коллекция пользователей (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3415fb7a2972621978ba3673343eb5f32b0eec1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885621"
---
# <a name="users-collection-adox"></a>Коллекция пользователей (ADOX)


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
> <P>Перед добавлением объекта <STRONG>пользователя</STRONG> в коллекцию <STRONG>пользователей</STRONG> объекта <STRONG>группы</STRONG> , объект <STRONG>пользователя</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекции <STRONG>пользователей</STRONG> из <STRONG>каталога</STRONG>.</P>


