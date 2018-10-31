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
ms.openlocfilehash: ccf9a88b427925528ce4e6a293d0b1351cef9883
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863950"
---
# <a name="create-table-statement-microsoft-access-sql"></a>Инструкция CREATE TABLE (Microsoft Access SQL)

**Применимо к**: Access 2013 | Office 2013

Создает новую таблицу.

> [!NOTE]
> Ядро СУБД Microsoft Access не поддерживает использование CREATE TABLE или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Access. Используйте методы **Создания DAO** .

## <a name="syntax"></a>Синтаксис

Создание \[ВРЕМЕННЫЕ\] таблицы в *таблице* (*Тип field1* \[(*размер*)\] \[NOT NULL\] \[с СЖАТИЕ | С помощью COMP\] \[ *ИНДЕКС1* \] \[, *поле2* *Тип* \[(*размер*)\] \[NOT NULL\] \[ *index2* \] \[,... \] \] \[, Ограничение *multifieldindex* \[,... \]\])

Инструкция CREATE TABLE состоит из следующих частей:

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
<td><p><em>table</em></p></td>
<td><p>Имя таблицы будет создан.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имя поля или поля, созданные в новую таблицу. Необходимо создать хотя бы одно поле.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Тип данных <em>поля</em> в новую таблицу.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em>.</p></td>
<td><p>Размер поля в знаках (только текст и двоичные поля).</p></td>
</tr>
<tr class="odd">
<td><p><em>ИНДЕКС1</em>, <em>index2</em></p></td>
<td><p>Определяет индекс по одному полю предложения ограничения. Дополнительные сведения о создании этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">предложение ограничения</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>Предложение ограничения, определяет составной индекс. Дополнительные сведения о создании этого индекса видеть <a href="constraint-clause-microsoft-access-sql.md">предложение ограничения</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Используйте инструкцию CREATE TABLE, чтобы определить новую таблицу, поля и ограничения полей. Если не указано значение NULL для поля, обязательно должно содержать допустимые данные в этих полях.

Предложение ограничения устанавливает различные ограничения на доступ к полю и можно использовать для создания основного ключа. Инструкция [CREATE INDEX](create-index-statement-microsoft-access-sql.md) можно также использовать для создания основного ключа или дополнительных индексов для существующих таблиц.

НЕ NULL можно использовать на одного поля или внутри именованного предложения ограничения для одного или для нескольких полей с именем ограничения. Тем не менее можно применить к полю ограничение NOT NULL только один раз. Попытка использовать это ограничение более одного раза приводит к ошибке времени выполнения.

При создании ВРЕМЕННОЙ таблицы, этот номер виден только в рамках сеанса, в котором он был создан. Автоматически удаляется при завершении сеанса. Доступ к временные таблицы может быть более одного пользователя.

Атрибут с СЖАТИЯ может использоваться только с символов и MEMO (также известной как текст) типы данных и синонимы.

Атрибут СЖАТИЯ с был добавлен для столбцов символов из-за изменения в формат представления символ Юникода. Символы Юникода требуется два байта для каждого символа. Для существующих баз данных Microsoft Jet, которые содержат преимущественно символ данные это означает, что файл базы данных практически в два раза и в размер при преобразовании формат ядра базы данных Microsoft Access. Тем не менее Юникод многих наборов знаков, которые ранее идентификаторами как однобайтовых знаков задает (их Изготовителей), можно легко сжатием на один байт. При определении столбца символ с помощью этого атрибута данных будут сжатию автоматически при сохранении и восстанавливаться при получении из столбца.

Также можно определить MEMO столбцов для хранения данных в сжатом формате. Однако существует ограничение. Только экземпляры MEMO столбцов, если сжат, помещается в 4096 байт или меньше, сжимаются. Все остальные экземпляры столбцов MEMO останутся в обычном состоянии. Это означает, что в указанной таблице, для определенного столбца ЗАМЕТКА может сжатием некоторые данные и не сжимаются некоторые данные.

## <a name="example"></a>Пример

В этом примере создается новая таблица с именем ThisTable с двух текстовых полей.

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

В этом примере создается новая таблица с именем MyTable с двух текстовых полей, поля даты/времени и уникальный индекс, состоящих из всех трех полей.

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

В этом примере создается новая таблица с двух текстовых полей и **целого** поля. В поле SSN — основной ключ.

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
