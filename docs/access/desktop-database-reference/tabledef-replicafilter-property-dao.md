---
title: TableDef.ReplicaFilter Property (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a5cc7394b01dcd79d17e3fcc7568bb8081ee12ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872643"
---
# <a name="tabledefreplicafilter-property-dao"></a>TableDef.ReplicaFilter Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение на объекте **[TableDef](tabledef-object-dao.md)** в реплику, которое указывает, какие подмножество записей реплицированы на таблицу с полной реплики. (Microsoft Access рабочие области только).

## <a name="syntax"></a>Синтаксис

*выражение* . Этого

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение — это **строка** или **типа Boolean** , которое указывает, какие подмножество записей репликации, как указано в следующей таблице:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Строка.</p></td>
<td><p>Критерии, по которым должны соответствовать записи в таблице реплику для реплицируемых из полной реплики.</p></td>
</tr>
<tr class="even">
<td><p><strong>Значение true</strong></p></td>
<td><p>Реплицирует все записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(По умолчанию) Не поддерживает репликацию записей.</p></td>
</tr>
</tbody>
</table>


Это свойство аналогично инструкцию SQL (без слова ГДЕ), однако нельзя указать вложенные запросы, статистические функции (такие как **Count**) или пользовательские функции критериям.

Можно синхронизировать только данные между полной реплики и частичные реплики. Синхронизация данных между двумя частичные реплики. Кроме того частичное репликации позволяет указать ограничения на которых реплицируются записей, но невозможно указать, какие поля будут реплицированы.

Как правило когда необходимо реплицировать на другой набор записей сбросить фильтр реплики. К примеру при торгового представителя временно переводит на другой торгового представителя область, приложения базы данных можно временно реплицировать данные для обеих областей и вернитесь к предыдущей фильтра. В этом сценарии приложение восстанавливаются значения по умолчанию **этого** и затем заполняет сокращенный реплики.

Если приложение изменяет реплики фильтры, необходимо выполните следующие действия.

1.  Используйте метод **[синхронизации](database-synchronize-method-dao.md)** для синхронизации с реплику, в котором изменяются фильтры полной реплики.

2.  Свойство **этого** внесите необходимые изменения в фильтр реплики.

3.  Метод **[PopulatePartial](database-populatepartial-method-dao.md)** используется для удаления всех записей из частичные реплики и перенести все записи с полной реплики, условиям фильтра новой реплики.

Чтобы удалить фильтр, задайте для **этого** значение **False**. Если вы не удалите все фильтры и вызвать метод **PopulatePartial** , записи не будут отображаться в любой реплицированной таблицы в частичные реплики.


> [!NOTE]
> <P>Если вызывается метод <STRONG>синхронизации</STRONG> без первого вызова <STRONG>PopulatePartial</STRONG>фильтр реплики была изменена, то перехватываемые возникает ошибка.</P>



## <a name="example"></a>Пример

В следующем примере **этого** реплицировать только записи клиентов из области Калифорния.

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

