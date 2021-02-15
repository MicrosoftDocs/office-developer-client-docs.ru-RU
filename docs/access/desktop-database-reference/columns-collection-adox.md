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

Содержит все [объекты Column](column-object-adox.md) таблицы, индекса или ключа.

## <a name="remarks"></a>Заметки

Метод [Append](append-method-adox-columns.md) для коллекции **Columns** уникален для ADOX. Вы можете выполнить указанные ниже действия.

  - Добавьте новый столбец в коллекцию с помощью **метода Append.**

Остальные свойства и методы являются стандартными для коллекций ADO. Вы можете выполнить указанные ниже действия.

  - Доступ к столбцу в коллекции с помощью [свойства Item.](item-property-ado.md)

  - Возвращает количество столбцов, содержащихся в коллекции, со свойством [Count.](count-property-ado.md)

  - Удалите столбец из коллекции с помощью метода [Delete.](delete-method-adox-collections.md)

  - Обновите объекты в коллекции, чтобы отразить схему текущей базы данных с помощью метода [Refresh.](refresh-method-ado.md)


> [!NOTE]
> Ошибка будет возникать при  приложении столбца к [](index-object-adox.md) коллекции **Columns** индекса, [](table-object-adox.md) если столбец не существует в таблице, которая уже была сдана в коллекцию [Tables.](tables-collection-adox.md) 


