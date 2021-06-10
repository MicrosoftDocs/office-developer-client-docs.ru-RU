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
# <a name="databasepopulatepartial-method-dao"></a><span data-ttu-id="f3976-102">Метод Database.PopulatePartial (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3976-102">Database.PopulatePartial method (DAO)</span></span>

<span data-ttu-id="f3976-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3976-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3976-104">Синхронизирует любые изменения частичной реплики с полной репликой, очищает все записи в частичной реплике, а затем повторно населяет частичную реплику на основе текущих фильтров реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-104">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters.</span></span> <span data-ttu-id="f3976-105">(только базы данных баз данных microsoft Access.).</span><span class="sxs-lookup"><span data-stu-id="f3976-105">(Microsoft Access database engine databases only.).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3976-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3976-106">Syntax</span></span>

<span data-ttu-id="f3976-107">*выражения* . PopulatePartial ***(DbPathName)***</span><span class="sxs-lookup"><span data-stu-id="f3976-107">*expression* .PopulatePartial(***DbPathName***)</span></span>

<span data-ttu-id="f3976-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="f3976-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3976-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3976-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3976-110">Имя</span><span class="sxs-lookup"><span data-stu-id="f3976-110">Name</span></span></p></th>
<th><p><span data-ttu-id="f3976-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="f3976-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f3976-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f3976-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="f3976-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f3976-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3976-114"><em>DbPathName</em></span><span class="sxs-lookup"><span data-stu-id="f3976-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="f3976-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f3976-115">Required</span></span></p></td>
<td><p><span data-ttu-id="f3976-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f3976-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f3976-117">Путь и имя полной реплики для заполнения записей.</span><span class="sxs-lookup"><span data-stu-id="f3976-117">The path and name of the full replica from which to populate records.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f3976-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3976-118">Remarks</span></span>

<span data-ttu-id="f3976-119">При синхронизации частичной реплики с полной репликой можно создать "осиротевших" записей в частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="f3976-119">When you synchronize a partial replica with a full replica, it is possible to create "orphaned" records in the partial replica.</span></span> <span data-ttu-id="f3976-120">Например, предположим, что у вас есть таблица Клиентов с ее **[репликойFilter](tabledef-replicafilter-property-dao.md)** с задаткой "Region = "CA".</span><span class="sxs-lookup"><span data-stu-id="f3976-120">For example, suppose you have a Customers table with its **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** set to "Region = 'CA'".</span></span> <span data-ttu-id="f3976-121">Если пользователь изменяет область клиента из ЦС в Нью-Йорк в частичной реплике, а затем происходит синхронизация с помощью метода **[Синхронизация,](database-synchronize-method-dao.md)** это изменение распространяется на полную реплику, но запись, содержащая NY в частичной реплике, осиротеет, так как теперь она не соответствует критериям фильтра реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-121">If a user changes a customer's region from CA to NY in the partial replica, and then a synchronization occurs via the **[Synchronize](database-synchronize-method-dao.md)** method, the change is propagated to the full replica but the record containing NY in the partial replica is orphaned because it now doesn't meet the replica filter criteria.</span></span>

<span data-ttu-id="f3976-122">Чтобы решить проблему осиротевших записей, можно использовать метод **PopulatePartial.**</span><span class="sxs-lookup"><span data-stu-id="f3976-122">To solve the problem of orphaned records, you can use the **PopulatePartial** method.</span></span> <span data-ttu-id="f3976-123">Метод **PopulatePartial** похож на метод **Синхронизация,** но он синхронизирует любые изменения с полной репликой, удаляет все записи в частичной реплике, а затем повторно заполняет частичную реплику на основе текущих фильтров реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-123">The **PopulatePartial** method is similar to the **Synchronize** method, but it synchronizes any changes with the full replica, removes all records in the partial replica, and then repopulates the partial replica based on the current replica filters.</span></span> <span data-ttu-id="f3976-124">Даже если фильтры реплики не изменились, **PopulatePartial** всегда будет очищать все записи в частичной реплике и населять ее на основе текущих фильтров.</span><span class="sxs-lookup"><span data-stu-id="f3976-124">Even if your replica filters have not changed, **PopulatePartial** will always clear all records in the partial replica and repopulate it based on the current filters.</span></span>

<span data-ttu-id="f3976-125">Обычно следует использовать метод **PopulatePartial** при создании частичной реплики и при изменении фильтров реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-125">Generally, you should use the **PopulatePartial** method when you create a partial replica and whenever you change your replica filters.</span></span> <span data-ttu-id="f3976-126">Если приложение меняет фильтры реплики, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f3976-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="f3976-127">Синхронизация полной реплики с частичной репликой, в которой меняются фильтры.</span><span class="sxs-lookup"><span data-stu-id="f3976-127">Synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="f3976-128">Используйте свойства **ReplicaFilter** и **[PartialReplica,](relation-partialreplica-property-dao.md)** чтобы внести нужные изменения в фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-128">Use the **ReplicaFilter** and **[PartialReplica](relation-partialreplica-property-dao.md)** properties to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="f3976-129">Вызов метода **PopulatePartial,** чтобы удалить все записи из частичной реплики и перенести все записи из полной реплики, которые соответствуют новым критериям фильтрации реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-129">Call the **PopulatePartial** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="f3976-130">Если фильтр реплики изменился, и метод **Синхронизация** вызывается без первого вызова **PopulatePartial,** возникает ошибка, которую можно оказаться в ловушке.</span><span class="sxs-lookup"><span data-stu-id="f3976-130">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

<span data-ttu-id="f3976-131">Метод **PopulatePartial** можно вызвать только на частичной реплике, которая была открыта для эксклюзивного доступа.</span><span class="sxs-lookup"><span data-stu-id="f3976-131">The **PopulatePartial** method can only be invoked on a partial replica that has been opened for exclusive access.</span></span> <span data-ttu-id="f3976-132">Кроме того, нельзя вызывать метод **PopulatePartial** из кода, запущенного в самой частичной реплике.</span><span class="sxs-lookup"><span data-stu-id="f3976-132">Furthermore, you can't call the **PopulatePartial** method from code running within the partial replica itself.</span></span> <span data-ttu-id="f3976-133">Вместо этого откройте частичную реплику исключительно из полной реплики или другой базы данных, а затем позвоните **в PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="f3976-133">Instead, open the partial replica exclusively from the full replica or another database, then call **PopulatePartial**.</span></span>


> [!NOTE]
> <span data-ttu-id="f3976-134">Хотя **PopulatePartial** выполняет одновую синхронизацию перед очисткой и перенаселением частичной реплики, перед вызовом **PopulatePartial** по-прежнему стоит вызвать синхронизацию. </span><span class="sxs-lookup"><span data-stu-id="f3976-134">Although **PopulatePartial** performs a one-way synchronization before clearing and repopulating the partial replica, it is still a good idea to call **Synchronize** before calling **PopulatePartial**.</span></span> <span data-ttu-id="f3976-135">Это происходит из-за того, что при сбойе вызова **синхронизации** возникает ошибка, которая может быть заблокирована.</span><span class="sxs-lookup"><span data-stu-id="f3976-135">This is because if the call to **Synchronize** fails, a trappable error occurs.</span></span> <span data-ttu-id="f3976-136">С помощью этой ошибки можно решить, следует ли использовать метод **PopulatePartial** (который удаляет все записи в частичной реплике).</span><span class="sxs-lookup"><span data-stu-id="f3976-136">You can use this error to decide whether or not to proceed with the **PopulatePartial** method (which removes all records in the partial replica).</span></span> <span data-ttu-id="f3976-137">Если **PopulatePartial** вызван сам по себе и во время синхронизации записей возникает ошибка, записи в частичной реплике будут по-прежнему очищаться, что может быть не желаемым результатом.</span><span class="sxs-lookup"><span data-stu-id="f3976-137">If **PopulatePartial** is called by itself and an error occurs while records are being synchronized, records in the partial replica will still be cleared, which may not be the desired result.</span></span>



## <a name="example"></a><span data-ttu-id="f3976-138">Пример</span><span class="sxs-lookup"><span data-stu-id="f3976-138">Example</span></span>

<span data-ttu-id="f3976-139">В следующем примере используется **метод PopulatePartial** после изменения фильтра реплики.</span><span class="sxs-lookup"><span data-stu-id="f3976-139">The following example uses the **PopulatePartial** method after changing a replica filter.</span></span>

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

