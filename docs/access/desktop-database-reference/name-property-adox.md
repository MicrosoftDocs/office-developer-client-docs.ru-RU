---
title: Свойство Name (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eab0b4b21f68f4facbd6b642aff4df5a328caad8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883115"
---
# <a name="name-property-adox"></a>Свойство Name (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение.

## <a name="remarks"></a>Замечания

Имена не обязательно должно быть уникальным в семействе сайтов.

Свойство **Name** — чтение и запись на [столбец](column-object-adox.md), [группы](group-object-adox.md), [ключа](key-object-adox.md), [индекса](index-object-adox.md), [таблицы](table-object-adox.md)и объектов- [пользователей](user-object-adox.md) . Свойство **Name** на объекты [каталога](catalog-object-adox.md), [процедуры](procedure-object-adox.md)и [представления](view-object-adox.md) только для чтения.

Для чтения и записи объектов (**столбец**, **группы**, **ключ**, **индекса**, **таблицы** и **пользователь** ), значение по умолчанию — пустая строка (»»).


> [!NOTE]
> <P>Для клавиш это свойство соответствует на объекты <STRONG>ключ</STRONG> уже добавляется в конец коллекции только для чтения.</P>




> [!NOTE]
> <P>Для таблиц это свойство доступно только для чтения для объектов <STRONG>в таблице</STRONG> , уже добавляется в конец коллекции.</P>


