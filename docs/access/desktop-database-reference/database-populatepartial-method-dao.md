---
title: Метод Database.PopulatePartial (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e0f77c356e0a13c2a1a83986a92c2b25029ecb4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294801"
---
# <a name="databasepopulatepartial-method-dao"></a>Метод Database.PopulatePartial (DAO)

**Область применения**: Access 2013, Office 2013

Синхронизирует любые изменения частичной реплики с полной репликой, очищает все записи в частичной реплике, а затем повторно населяет частичную реплику на основе текущих фильтров реплики. (только базы данных баз данных microsoft Access.).

## <a name="syntax"></a>Синтаксис

*выражения* . PopulatePartial ***(DbPathName)***

*выражение*: переменная, представляющая объект **Database**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Путь и имя полной реплики для заполнения записей.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

При синхронизации частичной реплики с полной репликой можно создать "осиротевших" записей в частичной реплике. Например, предположим, что у вас есть таблица Клиентов с ее **[репликойFilter](tabledef-replicafilter-property-dao.md)** с задаткой "Region = "CA". Если пользователь изменяет область клиента из ЦС в Нью-Йорк в частичной реплике, а затем происходит синхронизация с помощью метода **[Синхронизация,](database-synchronize-method-dao.md)** это изменение распространяется на полную реплику, но запись, содержащая NY в частичной реплике, осиротеет, так как теперь она не соответствует критериям фильтра реплики.

Чтобы решить проблему осиротевших записей, можно использовать метод **PopulatePartial.** Метод **PopulatePartial** похож на метод **Синхронизация,** но он синхронизирует любые изменения с полной репликой, удаляет все записи в частичной реплике, а затем повторно заполняет частичную реплику на основе текущих фильтров реплики. Даже если фильтры реплики не изменились, **PopulatePartial** всегда будет очищать все записи в частичной реплике и населять ее на основе текущих фильтров.

Обычно следует использовать метод **PopulatePartial** при создании частичной реплики и при изменении фильтров реплики. Если приложение меняет фильтры реплики, выполните следующие действия:

1.  Синхронизация полной реплики с частичной репликой, в которой меняются фильтры.

2.  Используйте свойства **ReplicaFilter** и **[PartialReplica,](relation-partialreplica-property-dao.md)** чтобы внести нужные изменения в фильтр реплики.

3.  Вызов метода **PopulatePartial,** чтобы удалить все записи из частичной реплики и перенести все записи из полной реплики, которые соответствуют новым критериям фильтрации реплики.

Если фильтр реплики изменился, и метод **Синхронизация** вызывается без первого вызова **PopulatePartial,** возникает ошибка, которую можно оказаться в ловушке.

Метод **PopulatePartial** можно вызвать только на частичной реплике, которая была открыта для эксклюзивного доступа. Кроме того, нельзя вызывать метод **PopulatePartial** из кода, запущенного в самой частичной реплике. Вместо этого откройте частичную реплику исключительно из полной реплики или другой базы данных, а затем позвоните **в PopulatePartial**.


> [!NOTE]
> Хотя **PopulatePartial** выполняет одновую синхронизацию перед очисткой и перенаселением частичной реплики, перед вызовом **PopulatePartial** по-прежнему стоит вызвать синхронизацию.  Это происходит из-за того, что при сбойе вызова **синхронизации** возникает ошибка, которая может быть заблокирована. С помощью этой ошибки можно решить, следует ли использовать метод **PopulatePartial** (который удаляет все записи в частичной реплике). Если **PopulatePartial** вызван сам по себе и во время синхронизации записей возникает ошибка, записи в частичной реплике будут по-прежнему очищаться, что может быть не желаемым результатом.



## <a name="example"></a>Пример

В следующем примере используется **метод PopulatePartial** после изменения фильтра реплики.

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

