---
<<<<<<< Название HEAD: TOCTitle свойство SQLState (ADO): свойство SQLState (ADO) === заголовок: свойство SQLState (ADO) TOCTitle: свойство SQLState (ADO)
>>>>>>> главные ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="sqlstate-property-ado"></a>SQLState Property (ADO)
=======
# <a name="sqlstate-property-ado"></a>Свойство SQLState (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает состояние SQL для того или иного объекта [ошибки](error-object-ado.md) .

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает **строковое** значение пяти символов, которая стандарту ANSI SQL и указывает код ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **SQLState** читать код ошибки пяти знаков, поставщик возвращает при возникновении ошибки во время обработки инструкции SQL. Например при использовании поставщик Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server, коды ошибок состояний SQL берутся из ODBC, основанные на ошибки, относящиеся к ODBC или на ошибки, которые создаются из Microsoft SQL Server, а затем сопоставляются с ODBC ошибки. Эти коды ошибок описаны в стандарте ANSI SQL, но может быть по-разному реализован различных источников данных.

