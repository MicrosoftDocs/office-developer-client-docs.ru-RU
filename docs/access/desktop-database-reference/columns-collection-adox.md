---
title: Коллекция столбцов (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49fa1bf77a66dbab829aff20ee666ae1a5082cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862220"
---
# <a name="columns-collection-adox"></a>Коллекция столбцов (ADOX)


**Применимо к**: Access 2013 | Office 2013

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


