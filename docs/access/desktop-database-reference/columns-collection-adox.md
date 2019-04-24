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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296208"
---
# <a name="columns-collection-adox"></a>Коллекция Columns (ADOX)


**Область применения**: Access 2013, Office 2013

Содержит все объекты [Column](column-object-adox.md) таблицы, индекса или ключа.

## <a name="remarks"></a>Замечания

Метод [append](append-method-adox-columns.md) для коллекции **Columns** уникален для ADOX. Вы можете выполнить указанные ниже действия.

  - Добавьте новый столбец в коллекцию с помощью метода **append** .

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

  - Доступ к столбцу в коллекции со свойством [Item](item-property-ado.md) .

  - Возвращает количество столбцов, которые содержит коллекция со свойством [Count](count-property-ado.md) .

  - Удаление столбца из коллекции с помощью метода [Delete](delete-method-adox-collections.md) .

  - Обновление объектов в коллекции в соответствии с схемой текущей базы данных с помощью метода [Refresh](refresh-method-ado.md) .


> [!NOTE]
> При добавлении **столбца** в коллекцию **Columns** [индекса](index-object-adox.md) , если он не существует в [таблице](table-object-adox.md) , которая уже **** добавлена в коллекцию [Tables](tables-collection-adox.md) , произойдет ошибка.


