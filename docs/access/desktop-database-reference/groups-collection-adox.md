---
title: Коллекция Groups (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7bd2519af3ea3c35d8cc32ef1ec31ea4f9efa1e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936674"
---
# <a name="groups-collection-adox"></a>Коллекция Groups (ADOX)

**Применимо к**: Access 2013, Office 2013

Содержит все хранимые объекты [групповой](group-object-adox.md) каталога или пользователя.

## <a name="remarks"></a>Примечания

Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

Метод [Append](append-method-adox-groups.md) для семейства сайтов **групп** является уникальным для ADOX. Вы можете выполнить указанные ниже действия.

- Добавление новой группы безопасности в коллекцию с помощью метода **Append** .

Остальные свойства и методы являются стандартными в семействах сайтов ADO. Вы можете выполнить указанные ниже действия.

- Доступ к группы в семействе сайтов с помощью свойства [элемента](item-property-ado.md) .

- Возвращает число групп, содержащихся в коллекции со свойством [Count](count-property-ado.md) .

- Удаление группы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

- Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.

> [!NOTE]
> Перед добавлением объекта **группы** в коллекцию **групп** объекта **пользователя** , объект **группы** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекцию **групп** **каталога**.


