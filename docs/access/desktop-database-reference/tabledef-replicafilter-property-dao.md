---
title: Свойство TableDef. Репликафилтер (DAO)
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
# <a name="tabledefreplicafilter-property-dao"></a>Свойство TableDef. Репликафилтер (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта **[tabledef](tabledef-object-dao.md)** в частичной реплике, которое указывает, какое подмножество записей реплицируется в эту таблицу из полной реплики. (Только для рабочих областей Microsoft Access.)

## <a name="syntax"></a>Синтаксис

*Expression* . репликафилтер

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

Параметр или возвращаемое значение — это **строка** или **логическое** значение, которое указывает, какое подмножество записей реплицируется, как указано в следующей таблице:

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
<td><p>Условие того, что запись в таблице частичной реплики должна удовлетворять, чтобы быть реплицированной из полной реплики.</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>Реплицирует все записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>Умолчани Не реплицирует записи.</p></td>
</tr>
</tbody>
</table>


Это свойство аналогично предложению WHERE SQL (без слова WHERE), но нельзя указать вложенные запросы, статистические функции (например, **Count**) или пользовательские функции в условиях.

Синхронизировать данные можно только между полной репликой и частичной репликой. Невозможно синхронизировать данные между двумя частичными репликами. Кроме того, с частичной репликацией можно установить ограничения на репликацию записей, но нельзя указать, какие поля будут реплицированы.

Обычно фильтр реплики сбрасывается, когда требуется реплицировать другой набор записей. Например, когда торговый представитель временно занимает другой регион торгового представителя, приложение базы данных может временно выполнить репликацию данных для обоих регионов, а затем вернуться к предыдущему фильтру. В этом сценарии приложение сбрасывает свойство **репликафилтер** , а затем повторно заполняет частичную реплику.

Если приложение изменяет фильтры реплики, выполните указанные ниже действия.

1.  С помощью метода **[Synchronize](database-synchronize-method-dao.md)** синхронизируйте всю реплику с частичной репликой, в которой изменяются фильтры.

2.  Используйте свойство **репликафилтер** , чтобы внести необходимые изменения в фильтр реплики.

3.  Используйте метод **[популатепартиал](database-populatepartial-method-dao.md)** , чтобы удалить все записи из частичной реплики и перенести все записи из полной реплики, соответствующие новым условиям фильтра реплики.

Чтобы удалить фильтр, присвойте свойству **Репликафилтер** **значение false**. Если удалить все фильтры и вызвать метод **популатепартиал** , никакие записи не будут отображаться ни в одной из реплицируемых таблиц в частичной реплике.

> [!NOTE]
> Если фильтр реплики изменился, а метод **Synchronize** вызывается без первого вызова **популатепартиал**, возникает перехватываемая ошибка.

## <a name="example"></a>Пример

В следующем примере используется свойство **репликафилтер** для репликации только записей клиентов из региона Калифорния.

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

