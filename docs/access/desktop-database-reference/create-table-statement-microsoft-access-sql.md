---
title: Инструкция CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706175"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Инструкция CREATE TABLE (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает таблицу.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование CREATE TABLE или любых других инструкций DDL с базами данных не на основе ядра СУБД Microsoft Access. Используйте вместо этого методы DAO **Create**.

## <a name="syntax"></a>Синтаксис

CREATE \[TEMPORARY\] TABLE *таблица* (*поле1 тип* \[(*размер*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*индекс1*\] \[, *поле2* *тип* \[(*размер*)\] \[NOT NULL\] \[*индекс2*\] \[, …\]\] \[, CONSTRAINT *индекс_набора_полей* \[, …\]\])

Инструкция CREATE TABLE включает в себя следующие элементы:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>таблица</em></p></td>
<td><p>Имя таблицы, которую требуется создать.</p></td>
</tr>
<tr class="even">
<td><p><em>поле1</em>, <em>поле2</em></p></td>
<td><p>Имена полей, которые создаются в новой таблице. Необходимо создать хотя бы одно поле.</p></td>
</tr>
<tr class="odd">
<td><p><em>тип</em></p></td>
<td><p>Тип данных <em>поля</em> в новой таблице.</p></td>
</tr>
<tr class="even">
<td><p><em>размер</em></p></td>
<td><p>Размер поля в знаках (только для полей с типом данных TEXT и BINARY).</p></td>
</tr>
<tr class="odd">
<td><p><em>индекс1</em>, <em>индекс2</em></p></td>
<td><p>Предложение CONSTRAINT, определяющее индекс по одному полю. Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>индекс_набора_полей</em></p></td>
<td><p>Предложение CONSTRAINT, определяющее индекс по нескольким полям. Дополнительные сведения о создании этого индекса см. в статье, посвященной <a href="constraint-clause-microsoft-access-sql.md">предложению CONSTRAINT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Используйте инструкцию CREATE TABLE, чтобы определить новую таблицу, поля и ограничения полей. Если для поля определено свойство NOT NULL, поле обязательно должно содержать допустимые данные.

Предложение CONSTRAINT накладывает на поле различные ограничения, и с помощью него можно задать первичный ключ. Для создания первичного ключа или дополнительных индексов в существующих таблицах можно использовать инструкцию [CREATE INDEX](create-index-statement-microsoft-access-sql.md).

Свойство NOT NULL можно задавать для одного поля или внутри именованного предложения CONSTRAINT для одного или нескольких полей. Свойство NOT NULL для поля можно задать только один раз. Попытка определить это свойство повторно приведет к ошибке выполнения.

Таблица, созданная с помощью атрибута TEMPORARY, доступна только в течение того сеанса, во время которого она была создана. Она автоматически удаляется по завершении сеанса. Несколько пользователей могут иметь доступ к временной таблице.

Атрибут WITH COMPRESSION можно использовать только с типами данных CHARACTER, MEMO (другое название — TEXT) и их синонимами.

Атрибут WITH COMPRESSION был добавлен для столбцов с типом данных CHARACTER из-за изменения формата представления знаков Юникода. Каждый знак Юникода всегда занимает два байта. Для существующих баз данных Microsoft Jet, содержащих преимущественно символьные данные, это может привести к почти двукратному увеличению размера при преобразовании в формат ядра СУБД Microsoft Access. Однако представление Юникода для многих наборов символов, которые прежде назывались однобайтовыми кодировками (SBCS), можно без труда сжать до одного байта на символ. Если для столбца с типом данных CHARACTER задать этот атрибут, при сохранении данные автоматически будут сжиматься, а при извлечении из столбца — возвращаться в исходное состояние.

Столбцы с типом данных MEMO также могут содержать сжатые данные. Однако в этом случае существует ограничение. Сжатию могут быть подвергнуты только те поля столбцов с типом данных MEMO, размер которых после сжатия не будет превышать 4096 байт. Остальные поля столбцов с типом данных MEMO останутся в обычном состоянии. Таким образом, в пределах одной таблицы и одного столбца с типом данных MEMO одни данные могут быть подвергнуты сжатию, а другие — нет.

## <a name="example"></a>Пример

В этом примере создается новая таблица с именем ThisTable и двумя текстовыми полями.

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

В этом примере создается новая таблица с именем MyTable с двумя текстовыми поля, полем даты и времени и уникальным индексом, состоящим из всех трех полей.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере создается новая таблица с двумя текстовыми полями и полем **Integer**. Поле SSN является первичным ключом.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере создается новая таблица с именем `~~Kitsch'n Sync`, в которой показаны различные типы полей и индексов. Поле счетчика является первичным ключом.

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
