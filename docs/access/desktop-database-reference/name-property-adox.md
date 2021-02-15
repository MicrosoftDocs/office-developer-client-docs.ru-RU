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

Задает или возвращает **строку.**

## <a name="remarks"></a>Заметки

Имена не должны быть уникальными в коллекции.

Свойство **Name можно** читать и записывать в [объектах Column,](column-object-adox.md) [Group,](group-object-adox.md) [Key,](key-object-adox.md) [Index,](index-object-adox.md) [Table](table-object-adox.md) [и User.](user-object-adox.md) Свойство **Name находится** в объектах [Catalog,](catalog-object-adox.md) [Procedure](procedure-object-adox.md)и [View только](view-object-adox.md) для чтения.

Для  объектов **"Столбец",** **"Группа",**"Ключ", **"Индекс",**  "Таблица" и "Пользователь" значение по умолчанию — пустая строка (""). 

> [!NOTE]
> - Для ключей это свойство доступно только для чтения в объектах **Key,** которые уже были приданы коллекции.
> - Для таблиц это свойство доступно только для чтения для объектов **Table,** которые уже были в коллекции.


