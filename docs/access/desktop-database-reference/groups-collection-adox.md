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

Содержит все сохраненные [объекты group](group-object-adox.md) каталога или пользователя.

## <a name="remarks"></a>Заметки

Коллекция **Groups** [каталога](catalog-object-adox.md) представляет все учетные записи группы каталога. Коллекция **Groups** для [пользователя представляет](user-object-adox.md) только группу, к которой принадлежит пользователь.

Метод [Append](append-method-adox-groups.md) для коллекции **Groups** уникален для ADOX. Вы можете выполнить указанные ниже действия.

- Добавьте новую группу безопасности в коллекцию с помощью **метода Append.**

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

- Доступ к группе в коллекции с помощью [свойства Item.](item-property-ado.md)

- Возвращает количество групп, содержащихся в коллекции, со свойством [Count.](count-property-ado.md)

- Удалите группу из коллекции с помощью метода [Delete.](delete-method-adox-collections.md)

- Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью метода [Refresh.](refresh-method-ado.md)

> [!NOTE]
> Прежде чем приместь объект [](name-property-adox.md) **Group** к коллекции **Groups** объекта **User,** объект **Group** с тем же именем, что и объект, который необходимо к ним примедить, должен уже существовать в коллекции **Groups** **каталога.**


