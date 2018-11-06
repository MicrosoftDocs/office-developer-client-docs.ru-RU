---
title: Свойство Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c66c4e6b8fc43a27b2feb87e45ec436e3abfa49
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998919"
---
# <a name="name-property-adox"></a>Свойство Name (ADOX)

**Применимо к**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение.

## <a name="remarks"></a>Примечания

Имена не обязательно должно быть уникальным в семействе сайтов.

Свойство **Name** — чтение и запись на [столбец](column-object-adox.md), [группы](group-object-adox.md), [ключа](key-object-adox.md), [индекса](index-object-adox.md), [таблицы](table-object-adox.md)и объектов- [пользователей](user-object-adox.md) . Свойство **Name** на объекты [каталога](catalog-object-adox.md), [процедуры](procedure-object-adox.md)и [представления](view-object-adox.md) только для чтения.

Для чтения и записи объектов (**столбец**, **группы**, **ключ**, **индекса**, **таблицы** и **пользователь** ), значение по умолчанию — пустая строка (»»).

> [!NOTE]
> - Для клавиш это свойство соответствует на объекты **ключ** уже добавляется в конец коллекции только для чтения.
> - Для таблиц это свойство доступно только для чтения для объектов **в таблице** , уже добавляется в конец коллекции.


