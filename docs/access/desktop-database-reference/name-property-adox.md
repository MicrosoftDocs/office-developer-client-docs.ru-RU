---
title: Свойство Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288653"
---
# <a name="name-property-adox"></a>Свойство Name (ADOX)

**Область применения**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение.

## <a name="remarks"></a>Примечания

Имена не обязательно должны быть уникальными в пределах коллекции.

Свойство **Name** доступно для чтения и записи в [столбцах](column-object-adox.md), [группах](group-object-adox.md), [ключах](key-object-adox.md), [индексе](index-object-adox.md), [таблице](table-object-adox.md)и [пользовательских](user-object-adox.md) объектах. Свойство **Name** доступно только для чтения в объектах [каталога](catalog-object-adox.md), [процедур](procedure-object-adox.md)и [представлений](view-object-adox.md) .

Для объектов чтения и записи (**столбец**, **Группа**, **ключ**, **индекс**, **Таблица** и **пользовательские** объекты) значением по умолчанию является пустая строка ("").

> [!NOTE]
> - Для ключей это свойство доступно только для чтения для объектов **Key** , уже добавленных в коллекцию.
> - Для таблиц это свойство доступно только для чтения для объектов **таблицы** , уже добавленных в коллекцию.


