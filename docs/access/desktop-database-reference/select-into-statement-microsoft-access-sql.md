---
title: SELECT.INTO Statement (Microsoft Access SQL)
TOCTitle: SELECT.INTO Statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4122421642b9746b5832984bf784faf65c603fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480338"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECT.INTO Statement (Microsoft Access SQL)


**Применимо к**: Access 2013 | Office 2013

Создает запрос на создание таблицы.

## <a name="syntax"></a>Синтаксис

Выбор *field1*\[, *поле2*\[,... \] \] В *новой_таблицы* \[в *внешняя_база_данных* \] из *источника*

Выбор... В оператор состоит из следующих частей:

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
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имя поля, которые копируются в новую таблицу.</p></td>
</tr>
<tr class="even">
<td><p><em>новой_таблицы</em></p></td>
<td><p>Имя таблицы будет создан. Он должен соответствовать типу стандартным соглашениям об именах. Если <em>новой_таблицы</em> совпадает с именем существующей таблицы, то перехватываемые возникает ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><em>внешняя_база_данных</em></p></td>
<td><p>Путь к внешней базе данных. Описание пути в разделе <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">в</a> предложение.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Имя существующей таблицы, из которой будут выбраны записи. Это может быть одной или нескольких таблиц или запроса.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Запросы на создание таблиц можно использовать для архивации записей, создания резервных копий таблиц или создания копий для экспорта в другую базу данных или для использования в качестве основы для отчетов, отображающих данные за определенный период времени. Например можно создать ежемесячные продажи региона отчета с помощью одного запроса создание таблицы каждый месяц.


> [!NOTE]
> <UL>
> <LI>
> <P>Можно определить первичный ключ для новой таблицы. При создании таблицы поля в новую таблицу наследование типа данных и поля размера каждое поле в таблицах запроса, но не другие поля или свойства таблицы данных.</P>
> <LI>
> <P>Добавление данных в существующую таблицу, используйте оператор <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A> для создания запроса на добавление.</P>
> <LI>
> <P>Чтобы узнать, какие записи будет установлен и перед запуском создание таблицы, сначала проверьте результаты <A href="select-statement-microsoft-access-sql.md">ВЫБЕРИТЕ</A> оператор, который использует же критерии выбора.</P></LI></UL>



## <a name="example"></a>Пример

В этом примере выбирает все записи в таблице сотрудников и копирует их в новую таблицу с именем экстренного резервного копирования.

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
