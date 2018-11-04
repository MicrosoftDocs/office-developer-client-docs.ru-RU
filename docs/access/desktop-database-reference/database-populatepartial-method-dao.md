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
ms.openlocfilehash: fc089ded79e9a25da566f44b668bf788d97fc4be
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949980"
---
# <a name="databasepopulatepartial-method-dao"></a>Метод Database.PopulatePartial (DAO)

**Применимо к**: Access 2013, Office 2013

Синхронизирует все изменения в частичные реплики с полной реплики, очищает все записи в частичные реплики и затем повторно заполняется реплику на основе текущего фильтров реплики. (База данных ядра базы данных Microsoft Access только.).

## <a name="syntax"></a>Синтаксис

*выражение* . PopulatePartial (***DbPathName***)

*выражение* Переменная, которая представляет собой объект **базы данных** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Путь и имя полной реплики, из которого для заполнения записей.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

При синхронизации частичные реплики с полной реплики, можно создать «потерянных» записей в частичные реплики. Допустим, у вас есть клиенты с его **[этого](tabledef-replicafilter-property-dao.md)** , задайте значение «область = «Центр сертификации»». При изменении пользователем региона клиента из центра сертификации для Нюнорск частичное реплики, а затем синхронизации с помощью метода **[синхронизации](database-synchronize-method-dao.md)** , изменения распределены по полной реплики, но запись, содержащую Нюнорск частичное реплики потерянные, так как теперь ИТ не соответствует условиям фильтра реплики.

Для решения проблемы потерянных записей, можно использовать метод **PopulatePartial** . Метод **PopulatePartial** похож на метод **синхронизации** , но синхронизирует все изменения с полной реплики, удаляются все записи в частичные реплики и затем повторно заполняется реплику на основе текущего фильтров реплики. Даже в том случае, если не были изменены фильтры реплики, **PopulatePartial** всегда снимите все записи в частичные реплики и повторного наполнения его на основе текущего фильтров.

Как правило следует использовать метод **PopulatePartial** при создании частичные реплики и при любом изменении фильтры реплики. Если приложение изменяет реплики фильтры, необходимо выполните следующие действия.

1.  Синхронизация полной реплики с реплику, в котором изменяются фильтры.

2.  Используйте **этого** и **[значений этих](relation-partialreplica-property-dao.md)** свойств для внесите необходимые изменения в фильтр реплики.

3.  Вызовите метод **PopulatePartial** , чтобы удалить все записи из частичные реплики и перенести все записи с полной реплики, условиям фильтра новой реплики.

Если вызывается метод **синхронизации** без первого вызова **PopulatePartial**фильтр реплики была изменена, то перехватываемые возникает ошибка.

Метод **PopulatePartial** может вызываться только на реплику, который был открыт для исключительного доступа. Кроме того не может вызывать метод **PopulatePartial** из кода, выполняющегося в рамках реплику самого. Вместо этого откройте реплику исключительно на основе полной реплики или другую базу данных, а затем вызывают **PopulatePartial**.


> [!NOTE]
> Несмотря на то, что **PopulatePartial** выполняет односторонней синхронизации перед Очистка и повторного заполнения частичные реплики, рекомендуется по-прежнему вызывать **синхронизировать** до вызова метода **PopulatePartial**. Это происходит в случае сбоя вызова **синхронизировать** перехватываемые ошибки. Следует ли продолжить работу с помощью метода **PopulatePartial** (который удаляет все записи в частичные реплики) можно использовать эту ошибку. Если возникает ошибка во время синхронизации записей **PopulatePartial** вызывается сам по себе, записей частичное реплики будет по-прежнему снят, могут быть результат.



## <a name="example"></a>Пример

В следующем примере метод **PopulatePartial** после изменения фильтра реплики.

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

