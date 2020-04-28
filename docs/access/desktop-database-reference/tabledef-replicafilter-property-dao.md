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
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="2f886-102">Свойство TableDef. Репликафилтер (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f886-102">TableDef.ReplicaFilter property (DAO)</span></span>

<span data-ttu-id="2f886-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f886-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f886-104">Задает или возвращает значение объекта **[tabledef](tabledef-object-dao.md)** в частичной реплике, которое указывает, какое подмножество записей реплицируется в эту таблицу из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="2f886-104">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica.</span></span> <span data-ttu-id="2f886-105">(Только для рабочих областей Microsoft Access.)</span><span class="sxs-lookup"><span data-stu-id="2f886-105">(Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f886-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f886-106">Syntax</span></span>

<span data-ttu-id="2f886-107">*Expression* . репликафилтер</span><span class="sxs-lookup"><span data-stu-id="2f886-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="2f886-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="2f886-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f886-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f886-109">Remarks</span></span>

<span data-ttu-id="2f886-110">Параметр или возвращаемое значение — это **строка** или **логическое** значение, которое указывает, какое подмножество записей реплицируется, как указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="2f886-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f886-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2f886-111">Value</span></span></p></th>
<th><p><span data-ttu-id="2f886-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2f886-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f886-113">Строка</span><span class="sxs-lookup"><span data-stu-id="2f886-113">A string</span></span></p></td>
<td><p><span data-ttu-id="2f886-114">Условие того, что запись в таблице частичной реплики должна удовлетворять, чтобы быть реплицированной из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="2f886-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f886-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="2f886-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="2f886-116">Реплицирует все записи.</span><span class="sxs-lookup"><span data-stu-id="2f886-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f886-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="2f886-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="2f886-118">Умолчани Не реплицирует записи.</span><span class="sxs-lookup"><span data-stu-id="2f886-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f886-119">Это свойство аналогично предложению WHERE SQL (без слова WHERE), но нельзя указать вложенные запросы, статистические функции (например, **Count**) или пользовательские функции в условиях.</span><span class="sxs-lookup"><span data-stu-id="2f886-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="2f886-120">Синхронизировать данные можно только между полной репликой и частичной репликой.</span><span class="sxs-lookup"><span data-stu-id="2f886-120">You can only synchronize data between a full replica and a partial replica.</span></span> <span data-ttu-id="2f886-121">Невозможно синхронизировать данные между двумя частичными репликами.</span><span class="sxs-lookup"><span data-stu-id="2f886-121">You can't synchronize data between two partial replicas.</span></span> <span data-ttu-id="2f886-122">Кроме того, с частичной репликацией можно установить ограничения на репликацию записей, но нельзя указать, какие поля будут реплицированы.</span><span class="sxs-lookup"><span data-stu-id="2f886-122">Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="2f886-123">Обычно фильтр реплики сбрасывается, когда требуется реплицировать другой набор записей.</span><span class="sxs-lookup"><span data-stu-id="2f886-123">Usually, you reset a replica filter when you want to replicate a different set of records.</span></span> <span data-ttu-id="2f886-124">Например, когда торговый представитель временно занимает другой регион торгового представителя, приложение базы данных может временно выполнить репликацию данных для обоих регионов, а затем вернуться к предыдущему фильтру.</span><span class="sxs-lookup"><span data-stu-id="2f886-124">For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter.</span></span> <span data-ttu-id="2f886-125">В этом сценарии приложение сбрасывает свойство **репликафилтер** , а затем повторно заполняет частичную реплику.</span><span class="sxs-lookup"><span data-stu-id="2f886-125">In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="2f886-126">Если приложение изменяет фильтры реплики, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2f886-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="2f886-127">С помощью метода **[Synchronize](database-synchronize-method-dao.md)** синхронизируйте всю реплику с частичной репликой, в которой изменяются фильтры.</span><span class="sxs-lookup"><span data-stu-id="2f886-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="2f886-128">Используйте свойство **репликафилтер** , чтобы внести необходимые изменения в фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="2f886-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="2f886-129">Используйте метод **[популатепартиал](database-populatepartial-method-dao.md)** , чтобы удалить все записи из частичной реплики и перенести все записи из полной реплики, соответствующие новым условиям фильтра реплики.</span><span class="sxs-lookup"><span data-stu-id="2f886-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="2f886-130">Чтобы удалить фильтр, присвойте свойству **Репликафилтер** **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2f886-130">To remove a filter, set the **ReplicaFilter** property to **False**.</span></span> <span data-ttu-id="2f886-131">Если удалить все фильтры и вызвать метод **популатепартиал** , никакие записи не будут отображаться ни в одной из реплицируемых таблиц в частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="2f886-131">If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>

> [!NOTE]
> <span data-ttu-id="2f886-132">Если фильтр реплики изменился, а метод **Synchronize** вызывается без первого вызова **популатепартиал**, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f886-132">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="2f886-133">Пример</span><span class="sxs-lookup"><span data-stu-id="2f886-133">Example</span></span>

<span data-ttu-id="2f886-134">В следующем примере используется свойство **репликафилтер** для репликации только записей клиентов из региона Калифорния.</span><span class="sxs-lookup"><span data-stu-id="2f886-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

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

