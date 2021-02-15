---
title: Свойство TableDef.ReplicaFilter (DAO)
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
localization_priority: Normal
ms.openlocfilehash: ba296701faebb32696741a742b7fe01660b74c46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302788"
---
# <a name="tabledefreplicafilter-property-dao"></a>Свойство TableDef.ReplicaFilter (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта **[TableDef](tabledef-object-dao.md)** в частичной реплике, которое указывает, какое подмножество записей реплицируется в эту таблицу из полной реплики. (Только для рабочих областей Microsoft Access.)

## <a name="syntax"></a>Синтаксис

*выражение .* ReplicaFilter

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

Параметром или возвращаемой величиной является **строка** или значение **boolean,** которое указывает, какое подмножество записей реплицируется, как указано в следующей таблице:

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
<td><p>Строка</p></td>
<td><p>Критерий, которым должна соответствовать запись в таблице частичной реплики для репликации из полной реплики.</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>Реплицирует все записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(По умолчанию) Не реплицирует записи.</p></td>
</tr>
</tbody>
</table>


Это свойство аналогично предложению SQL WHERE (без слова WHERE), но в критерии нельзя указывать вики-функции, агрегатные функции (например, count) или пользовательские функции.

Данные можно синхронизировать только между полной и частичной репликами. Данные нельзя синхронизировать между двумя частичными репликами. Кроме того, при частичной репликации можно установить ограничения на репликацию записей, но нельзя указать, какие поля реплицированы.

Обычно фильтр реплик сбрасывается, когда необходимо реплицировать другой набор записей. Например, когда представитель отдела продаж временно берет на себя контроль над регионом другого представителя, приложение базы данных может временно реплицировать данные для обоих регионов, а затем вернуться к предыдущему фильтру. В этом сценарии приложение сбрасывает свойство **ReplicaFilter,** а затем повторно насылает частичную реплику.

Если приложение изменяет фильтры реплик, выполните следующие действия.

1.  Используйте метод **[Synchronize](database-synchronize-method-dao.md)** для синхронизации полной реплики с частичной репликой, в которой меняются фильтры.

2.  Используйте свойство **ReplicaFilter,** чтобы внести нужные изменения в фильтр реплики.

3.  Используйте метод **[PopulatePartial](database-populatepartial-method-dao.md)** для удаления всех записей из частичной реплики и передачи всех записей из полной реплики, которые соответствуют новым критериям фильтра реплики.

Чтобы удалить фильтр, установите для свойства **ReplicaFilter** свойство **False.** Если удалить все фильтры и вызвать метод **PopulatePartial,** никакие записи не будут отображаться в реплицируемых таблицах в частичной реплике.

> [!NOTE]
> Если фильтр реплики изменился, а метод **Synchronize** вызывается без вызова **PopulatePartial,** возникает перехожимая ошибка.

## <a name="example"></a>Пример

В следующем примере свойство **ReplicaFilter** используется для репликации только записей клиентов из региона Калифорнии.

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

