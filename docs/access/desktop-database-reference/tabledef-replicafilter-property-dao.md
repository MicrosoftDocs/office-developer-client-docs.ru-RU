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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722433"
---
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="b3154-102">Свойство TableDef.ReplicaFilter (DAO)</span><span class="sxs-lookup"><span data-stu-id="b3154-102">TableDef.ReplicaFilter property (DAO)</span></span>

<span data-ttu-id="b3154-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3154-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3154-104">Задает или возвращает значение на объекте **[TableDef](tabledef-object-dao.md)** в реплику, которое указывает, какие подмножество записей реплицированы на таблицу с полной реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-104">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica.</span></span> <span data-ttu-id="b3154-105">(Microsoft Access рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="b3154-105">(Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3154-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3154-106">Syntax</span></span>

<span data-ttu-id="b3154-107">*выражение* . Этого</span><span class="sxs-lookup"><span data-stu-id="b3154-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="b3154-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="b3154-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3154-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3154-109">Remarks</span></span>

<span data-ttu-id="b3154-110">Параметр или возвращаемое значение — это **строка** или **типа Boolean** , которое указывает, какие подмножество записей репликации, как указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="b3154-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3154-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b3154-111">Value</span></span></p></th>
<th><p><span data-ttu-id="b3154-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b3154-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3154-113">Строка.</span><span class="sxs-lookup"><span data-stu-id="b3154-113">A string</span></span></p></td>
<td><p><span data-ttu-id="b3154-114">Критерии, по которым должны соответствовать записи в таблице реплику для реплицируемых из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3154-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="b3154-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="b3154-116">Реплицирует все записи.</span><span class="sxs-lookup"><span data-stu-id="b3154-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3154-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="b3154-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="b3154-118">(По умолчанию) Не поддерживает репликацию записей.</span><span class="sxs-lookup"><span data-stu-id="b3154-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3154-119">Это свойство аналогично инструкцию SQL (без слова ГДЕ), однако нельзя указать вложенные запросы, статистические функции (такие как **Count**) или пользовательские функции критериям.</span><span class="sxs-lookup"><span data-stu-id="b3154-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="b3154-120">Можно синхронизировать только данные между полной реплики и частичные реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-120">You can only synchronize data between a full replica and a partial replica.</span></span> <span data-ttu-id="b3154-121">Синхронизация данных между двумя частичные реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-121">You can't synchronize data between two partial replicas.</span></span> <span data-ttu-id="b3154-122">Кроме того частичное репликации позволяет указать ограничения на которых реплицируются записей, но невозможно указать, какие поля будут реплицированы.</span><span class="sxs-lookup"><span data-stu-id="b3154-122">Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="b3154-123">Как правило когда необходимо реплицировать на другой набор записей сбросить фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-123">Usually, you reset a replica filter when you want to replicate a different set of records.</span></span> <span data-ttu-id="b3154-124">К примеру при торгового представителя временно переводит на другой торгового представителя область, приложения базы данных можно временно реплицировать данные для обеих областей и вернитесь к предыдущей фильтра.</span><span class="sxs-lookup"><span data-stu-id="b3154-124">For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter.</span></span> <span data-ttu-id="b3154-125">В этом сценарии приложение восстанавливаются значения по умолчанию **этого** и затем заполняет сокращенный реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-125">In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="b3154-126">Если приложение изменяет реплики фильтры, необходимо выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b3154-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="b3154-127">Используйте метод **[синхронизации](database-synchronize-method-dao.md)** для синхронизации с реплику, в котором изменяются фильтры полной реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="b3154-128">Свойство **этого** внесите необходимые изменения в фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="b3154-129">Метод **[PopulatePartial](database-populatepartial-method-dao.md)** используется для удаления всех записей из частичные реплики и перенести все записи с полной реплики, условиям фильтра новой реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="b3154-130">Чтобы удалить фильтр, задайте для **этого** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="b3154-130">To remove a filter, set the **ReplicaFilter** property to **False**.</span></span> <span data-ttu-id="b3154-131">Если вы не удалите все фильтры и вызвать метод **PopulatePartial** , записи не будут отображаться в любой реплицированной таблицы в частичные реплики.</span><span class="sxs-lookup"><span data-stu-id="b3154-131">If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>

> [!NOTE]
> <span data-ttu-id="b3154-132">Если вызывается метод **синхронизации** без первого вызова **PopulatePartial**фильтр реплики была изменена, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b3154-132">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="b3154-133">Пример</span><span class="sxs-lookup"><span data-stu-id="b3154-133">Example</span></span>

<span data-ttu-id="b3154-134">В следующем примере **этого** реплицировать только записи клиентов из области Калифорния.</span><span class="sxs-lookup"><span data-stu-id="b3154-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

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

