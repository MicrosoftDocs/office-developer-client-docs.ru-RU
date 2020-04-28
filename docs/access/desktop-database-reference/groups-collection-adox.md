---
title: Коллекция Groups (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21f1880a9effca6e51bc1e8b52a58dce22ce1ea9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292078"
---
# <a name="groups-collection-adox"></a>Коллекция Groups (ADOX)

**Область применения**: Access 2013, Office 2013

Содержит все объекты [группы](group-object-adox.md) , хранящиеся в каталоге или пользователе.

## <a name="remarks"></a>Примечания

Коллекция **Groups** [каталога](catalog-object-adox.md) представляет все учетные записи групп в каталоге. Коллекция **Groups** для [пользователя](user-object-adox.md) представляет только группу, к которой принадлежит пользователь.

Метод [append](append-method-adox-groups.md) коллекции **GROUPS** уникален для ADOX. Вы можете выполнить указанные ниже действия.

- Добавьте новую группу безопасности в коллекцию с помощью метода **append** .

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

- Доступ к группе в коллекции со свойством [Item](item-property-ado.md) .

- Возвращает количество групп, содержащиеся в коллекции, со свойством [Count](count-property-ado.md) .

- Удаление группы из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

- Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .

> [!NOTE]
> Перед добавлением объекта **Group** в коллекцию **Groups** объекта **User** объект **Group** с тем же [именем](name-property-adox.md) , что и у добавляемого объекта, должен уже существовать в коллекции **Groups** **каталога**.


