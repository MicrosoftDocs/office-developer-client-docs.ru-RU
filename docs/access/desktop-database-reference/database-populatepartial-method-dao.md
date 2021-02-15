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

Синхронизирует все изменения в частичной реплике с полной репликой, очищает все записи в частичной реплике, а затем повторно наполнение частичной реплики на основе текущих фильтров реплики. (Только для баз данных ям баз данных Microsoft Access.)

## <a name="syntax"></a>Синтаксис

*выражение .* PopulatePartial(***DbPathName***)

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
<td><p>Обязательно</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Путь и имя полной реплики, из которой необходимо заполнить записи.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

При синхронизации частичной реплики с полной репликой можно создать «потерянные» записи в частичной реплике. Например, предположим, что у вас есть таблица Customers, для ее **[replicaFilter](tabledef-replicafilter-property-dao.md)** задав "Region = 'CA'". Если пользователь изменяет регион клиента с CA на NY в частичной реплике, а затем синхронизация происходит с помощью метода **[Synchronize,](database-synchronize-method-dao.md)** это изменение распространяется на полную реплику, но запись, содержащая НЬЮ-имя в частичной реплике, будет потерянным, так как теперь она не соответствует критериям фильтра реплики.

Для решения проблемы потерянных записей можно использовать метод **PopulatePartial.** Метод **PopulatePartial** похож на метод **Synchronize,** но синхронизирует все изменения с полной репликой, удаляет все записи в частичной реплике, а затем повторно заполняет частичную реплику на основе текущих фильтров реплики. Даже если ваши фильтры реплики не изменились, **PopulatePartial** всегда очищает все записи в частичной реплике и повторно заполняет их на основе текущих фильтров.

Как правило, метод **PopulatePartial** следует использовать при создании частичной реплики и при изменении фильтров реплики. Если приложение изменяет фильтры реплик, выполните следующие действия.

1.  Синхронизировать полную реплику с частичной репликой, в которой меняются фильтры.

2.  Используйте свойства **ReplicaFilter** и **[PartialReplica,](relation-partialreplica-property-dao.md)** чтобы внести нужные изменения в фильтр реплики.

3.  Вызовите **метод PopulatePartial,** чтобы удалить все записи из частичной реплики и передать все записи из полной реплики, которые соответствуют новым критериям фильтра реплики.

Если фильтр реплики изменился, а метод **Synchronize** вызывается без вызова **populatePartial,** возникает перехожимая ошибка.

Метод **PopulatePartial** можно вызвать только для частичной реплики, открытой для монопольного доступа. Кроме того, нельзя вызвать метод **PopulatePartial** из кода, запущенного в самой частичной реплике. Вместо этого откройте частичную реплику исключительно из полной реплики или другой базы данных, а затем вызовите **PopulatePartial.**


> [!NOTE]
> Хотя **PopulatePartial** выполняет однонаправленную синхронизацию перед очисткой и повторное заполнение частичной реплики, по-прежнему имеется хорошая идея вызвать **synchronize** перед вызовом **PopulatePartial**. Это происходит потому, что в случае с ошибки вызова **синхронизации** возникает перехронизируемый сбой. Эту ошибку можно использовать, чтобы решить, следует ли продолжать использование метода **PopulatePartial** (который удаляет все записи в частичной реплике). Если **populatePartial** вызван сам по себе и во время синхронизации записей возникает ошибка, записи в частичной реплике будут по-прежнему очищаться, что может оказаться не нужным результатом.



## <a name="example"></a>Пример

В следующем примере используется метод **PopulatePartial** после изменения фильтра реплики.

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

