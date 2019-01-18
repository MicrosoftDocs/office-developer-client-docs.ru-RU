---
title: Коллекция Columns (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720487"
---
# <a name="columns-collection-adox"></a>Коллекция Columns (ADOX)


**Применимо к**: Access 2013, Office 2013

Содержит все объекты [столбец](column-object-adox.md) таблицы, индекса или ключа.

## <a name="remarks"></a>Замечания

Метод [Append](append-method-adox-columns.md) для коллекции **столбцов** является уникальным для ADOX. Вы можете выполнить указанные ниже действия.

  - Добавление нового столбца в коллекцию с помощью метода **Append** .

Остальные свойства и методы являются стандартными в семействах сайтов ADO. Вы можете выполнить указанные ниже действия.

  - Доступ к столбца в коллекции с помощью свойства [элемента](item-property-ado.md) .

  - Возвращает число столбцов, содержащихся в коллекции со свойством [Count](count-property-ado.md) .

  - Удаление столбца из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

  - Обновление объектов в коллекции в соответствии с помощью метода [обновления на](refresh-method-ado.md) схему текущей базы данных.


> [!NOTE]
> После добавления **столбцов** в коллекцию **столбцов** [индекса](index-object-adox.md) , если **Столбец** не существует в [таблице](table-object-adox.md) , уже добавлен в коллекцию [таблиц](tables-collection-adox.md) , произойдет ошибка.


