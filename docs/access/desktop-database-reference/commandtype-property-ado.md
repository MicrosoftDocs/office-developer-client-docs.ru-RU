---
<<<<<<< Название HEAD: TOCTitle свойство CommandType (ADO): свойство CommandType (ADO) === название: свойства CommandType (ADO) TOCTitle: свойства CommandType (ADO)
>>>>>>> главные ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15) ms:contentKeyID: 48547663 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231125 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="commandtype-property-ado"></a>Свойства CommandType (ADO)
=======
# <a name="commandtype-property-ado"></a>Свойство CommandType (ADO)
>>>>>>> образец


**Применимо к**: Access 2013 | Office 2013

Указывает тип объекта [команды](command-object-ado.md) .

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> образец

Задает или возвращает одно или несколько значений [CommandTypeEnum](commandtypeenum.md) .

> [!NOTE]
> Не используйте значения **CommandTypeEnum** **adCmdFile** или **adCmdTableDirect** с **CommandType**. Эти значения может использоваться только как параметры методов [Open](open-method-ado-recordset.md) и [повторный запрос](requery-method-ado.md) набора [записей](recordset-object-ado.md).


## <a name="remarks"></a>Замечания

Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText](commandtext-property-ado.md) .

<<<<<<< HEAD, если значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), могут возникнуть снижение производительности, так как ADO необходимо выполнять вызовы к поставщику для определения **CommandText** свойство является инструкции SQL, хранимую процедуру или имя таблицы. Если вы знаете, какой тип используется, задав свойство **CommandType** команда указывает ADO для перехода в соответствующий код. Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText** , возникает ошибка при вызове метода [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) .
=== Значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), может привести к снижению производительности, так как ADO необходимо выполнять вызовы к поставщику, чтобы определить свойство **CommandText** инструкции SQL Хранимая процедура, или имя таблицы. Если вы знаете, какой тип используется, задав свойство **CommandType** команда указывает ADO для перехода в соответствующий код. Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText** , возникает ошибка при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .
>>>>>>> образец

