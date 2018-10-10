---
title: Columns Collection (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482583"
---
# <a name="columns-collection-adox"></a>Columns Collection (ADOX)


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
> <P>После добавления <STRONG>столбцов</STRONG> в коллекцию <STRONG>столбцов</STRONG> <A href="index-object-adox.md">индекса</A> , если <STRONG>Столбец</STRONG> не существует в <A href="table-object-adox.md">таблице</A> , уже добавлен в коллекцию <A href="tables-collection-adox.md">таблиц</A> , произойдет ошибка.</P>


