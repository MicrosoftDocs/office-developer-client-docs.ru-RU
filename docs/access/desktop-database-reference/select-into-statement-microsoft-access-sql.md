---
title: Инструкция SELECT.INTO (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308724"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>Инструкция SELECT.INTO (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает запрос на создание таблицы.

## <a name="syntax"></a>Синтаксис

SELECT *поле1*\[, *поле2*\[, …\]\] INTO *новая_таблица* \[IN *внешняя_база_данных*\] FROM *источник*

Инструкция SELECT...INTO состоит из следующих элементов:

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
<td><p><em>поле1</em>, <em>поле2</em></p></td>
<td><p>Имена полей, которые требуется скопировать в новую таблицу.</p></td>
</tr>
<tr class="even">
<td><p><em>новая_таблица</em></p></td>
<td><p>Имя таблицы, которую требуется создать. Необходимо соблюдать стандартные соглашения об именовании. При совпадении имен <em>новой_таблицы</em> и существующей таблицы возникает перехватываемая ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><em>внешняя_база_данных</em></p></td>
<td><p>Путь к внешней базе данных. Описание пути см. в статье, посвященной предложению <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>источник</em></p></td>
<td><p>Имя существующей таблицы, из которой отбираются записи. Источником может быть одна или несколько таблиц, а также запрос.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Запросы на создание таблиц можно использовать для архивации записей, для создания резервных копий таблиц, а также для создания копий с целью экспорта в другую базу данных или формирования отчетов, отображающих данные за определенный период времени. Например, отчет "Ежемесячные продажи по регионам" можно составлять, выполняя каждый месяц один и тот же запрос на создание таблиц.

> [!NOTE]
> - Может возникнуть необходимость определить первичный ключ для новой таблицы. При создании таблицы ее поля наследуют тип данных и размеры полей базовых таблиц запроса. Другие параметры полей не переносятся.
> - Чтобы добавить данные в таблицу, используйте вместо запроса на добавление инструкцию [INSERT INTO](insert-into-statement-microsoft-access-sql.md).
> - Чтобы определить, какие записи будут отобраны, до выполнения запроса на создание таблицы, сначала проверьте результат инструкции [SELECT](select-statement-microsoft-access-sql.md) с такими же условиями отбора.



## <a name="example"></a>Пример

В этом примере отбираются все записи в таблице Employees, которые копируются в новую таблицу Emp Backup.

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
