---
title: Семейство Groups (ADOX)
TOCTitle: Groups Collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 099b9b4034d64f768513cfa5c9a28b89bef89ef8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880994"
---
# <a name="groups-collection-adox"></a>Семейство Groups (ADOX)


**Применимо к**: Access 2013, Office 2013

Содержит все хранимые объекты [групповой](group-object-adox.md) каталога или пользователя.

## <a name="remarks"></a>Замечания

Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

Метод [Append](append-method-adox-groups.md) для семейства сайтов **групп** является уникальным для ADOX. Вы можете выполнить указанные ниже действия.

  - Добавление новой группы безопасности в коллекцию с помощью метода **Append** .

Остальные свойства и методы являются стандартными в семействах сайтов ADO. Вы можете выполнить указанные ниже действия.

  - Доступ к группы в семействе сайтов с помощью свойства [элемента](item-property-ado.md) .

  - Возвращает число групп, содержащихся в коллекции со свойством [Count](count-property-ado.md) .

  - Удаление группы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

  - Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.


> [!NOTE]
> <P>Перед добавлением объекта <STRONG>группы</STRONG> в коллекцию <STRONG>групп</STRONG> объекта <STRONG>пользователя</STRONG> , объект <STRONG>группы</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекцию <STRONG>групп</STRONG> <STRONG>каталога</STRONG>.</P>


