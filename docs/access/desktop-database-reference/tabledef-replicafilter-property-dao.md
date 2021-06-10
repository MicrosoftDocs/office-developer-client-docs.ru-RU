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
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="7be3b-102">Свойство TableDef.ReplicaFilter (DAO)</span><span class="sxs-lookup"><span data-stu-id="7be3b-102">TableDef.ReplicaFilter property (DAO)</span></span>

<span data-ttu-id="7be3b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7be3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7be3b-104">Задает или возвращает значение объекта **[TableDef](tabledef-object-dao.md)** в частичной реплике, которая указывает, какой подмножество записей реплицируется в эту таблицу из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="7be3b-104">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica.</span></span> <span data-ttu-id="7be3b-105">(Только для рабочих областей Microsoft Access.)</span><span class="sxs-lookup"><span data-stu-id="7be3b-105">(Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7be3b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7be3b-106">Syntax</span></span>

<span data-ttu-id="7be3b-107">*выражения* . ReplicaFilter</span><span class="sxs-lookup"><span data-stu-id="7be3b-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="7be3b-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="7be3b-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be3b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7be3b-109">Remarks</span></span>

<span data-ttu-id="7be3b-110">Значение параметра или возврата — **строка** или **boolean,** которые указывают, какая часть записей реплицируется, как указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="7be3b-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7be3b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7be3b-111">Value</span></span></p></th>
<th><p><span data-ttu-id="7be3b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7be3b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7be3b-113">Строка</span><span class="sxs-lookup"><span data-stu-id="7be3b-113">A string</span></span></p></td>
<td><p><span data-ttu-id="7be3b-114">Критерий, который должна соответствовать запись в частичной таблице реплики, чтобы реплицироваться из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="7be3b-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7be3b-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="7be3b-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="7be3b-116">Реплицирует все записи.</span><span class="sxs-lookup"><span data-stu-id="7be3b-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7be3b-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="7be3b-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="7be3b-118">(По умолчанию) Не реплицирует записи.</span><span class="sxs-lookup"><span data-stu-id="7be3b-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7be3b-119">Это свойство аналогично пункту SQL WHERE (без слова WHERE), но нельзя указать подквеи, агрегированные функции (например, **Count)** или функции, определенные пользователем в рамках критериев.</span><span class="sxs-lookup"><span data-stu-id="7be3b-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="7be3b-120">Можно синхронизировать данные только между полной репликой и частичной репликой.</span><span class="sxs-lookup"><span data-stu-id="7be3b-120">You can only synchronize data between a full replica and a partial replica.</span></span> <span data-ttu-id="7be3b-121">Нельзя синхронизировать данные между двумя частичными репликами.</span><span class="sxs-lookup"><span data-stu-id="7be3b-121">You can't synchronize data between two partial replicas.</span></span> <span data-ttu-id="7be3b-122">Кроме того, при частичной репликации можно установить ограничения на репликацию записей, но нельзя указать, какие поля реплицированы.</span><span class="sxs-lookup"><span data-stu-id="7be3b-122">Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="7be3b-123">Обычно при воспроизведении другого набора записей сбросить фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="7be3b-123">Usually, you reset a replica filter when you want to replicate a different set of records.</span></span> <span data-ttu-id="7be3b-124">Например, когда представитель отдела продаж временно берет на себя область другого представителя продаж, приложение базы данных может временно реплицировать данные для обоих регионов, а затем вернуться к предыдущему фильтру.</span><span class="sxs-lookup"><span data-stu-id="7be3b-124">For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter.</span></span> <span data-ttu-id="7be3b-125">В этом сценарии приложение сбрасывает свойство **ReplicaFilter,** а затем повторно населяет частичную реплику.</span><span class="sxs-lookup"><span data-stu-id="7be3b-125">In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="7be3b-126">Если приложение меняет фильтры реплики, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7be3b-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="7be3b-127">Используйте метод **[Синхронизация](database-synchronize-method-dao.md)** для синхронизации полной реплики с частичной репликой, в которой меняются фильтры.</span><span class="sxs-lookup"><span data-stu-id="7be3b-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="7be3b-128">Используйте свойство **ReplicaFilter,** чтобы внести нужные изменения в фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="7be3b-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="7be3b-129">Используйте метод **[PopulatePartial,](database-populatepartial-method-dao.md)** чтобы удалить все записи из частичной реплики и перенести все записи из полной реплики, которые соответствуют новым критериям фильтрации реплики.</span><span class="sxs-lookup"><span data-stu-id="7be3b-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="7be3b-130">Чтобы удалить фильтр, установите свойство **ReplicaFilter** **false**.</span><span class="sxs-lookup"><span data-stu-id="7be3b-130">To remove a filter, set the **ReplicaFilter** property to **False**.</span></span> <span data-ttu-id="7be3b-131">Если удалить все фильтры и вызвать метод **PopulatePartial,** записи не будут отображаться в каких-либо реплицируемых таблицах в частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="7be3b-131">If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>

> [!NOTE]
> <span data-ttu-id="7be3b-132">Если фильтр реплики изменился, и метод **Синхронизация** вызывается без первого вызова **PopulatePartial,** возникает ошибка, которую можно оказаться в ловушке.</span><span class="sxs-lookup"><span data-stu-id="7be3b-132">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="7be3b-133">Пример</span><span class="sxs-lookup"><span data-stu-id="7be3b-133">Example</span></span>

<span data-ttu-id="7be3b-134">В следующем примере свойство **ReplicaFilter** реплицирует только записи клиентов из региона Калифорния.</span><span class="sxs-lookup"><span data-stu-id="7be3b-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

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

