---
title: Инструкция CREATE TABLE (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295361"
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
