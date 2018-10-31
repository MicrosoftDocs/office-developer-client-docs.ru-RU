---
title: Database.PopulatePartial Method (DAO)
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
ms.openlocfilehash: fa52050e91c1a291dd59f9cde1ea36c320406dd6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860268"
---
# <a name="databasepopulatepartial-method-dao"></a><span data-ttu-id="13610-102">Database.PopulatePartial Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="13610-102">Database.PopulatePartial Method (DAO)</span></span>


<span data-ttu-id="13610-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="13610-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="13610-104">Синхронизирует все изменения в частичные реплики с полной реплики, очищает все записи в частичные реплики и затем повторно заполняется реплику на основе текущего фильтров реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-104">Synchronizes any changes in a partial replica with the full replica, clears all records in the partial replica, and then repopulates the partial replica based on the current replica filters.</span></span> <span data-ttu-id="13610-105">(База данных ядра базы данных Microsoft Access только.).</span><span class="sxs-lookup"><span data-stu-id="13610-105">(Microsoft Access database engine databases only.).</span></span>

## <a name="syntax"></a><span data-ttu-id="13610-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13610-106">Syntax</span></span>

<span data-ttu-id="13610-107">*выражение* . PopulatePartial (***DbPathName***)</span><span class="sxs-lookup"><span data-stu-id="13610-107">*expression* .PopulatePartial(***DbPathName***)</span></span>

<span data-ttu-id="13610-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="13610-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="13610-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="13610-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13610-110">Имя</span><span class="sxs-lookup"><span data-stu-id="13610-110">Name</span></span></p></th>
<th><p><span data-ttu-id="13610-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="13610-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="13610-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="13610-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="13610-113">Описание</span><span class="sxs-lookup"><span data-stu-id="13610-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13610-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="13610-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="13610-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13610-115">Required</span></span></p></td>
<td><p><span data-ttu-id="13610-116"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="13610-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="13610-117">Путь и имя полной реплики, из которого для заполнения записей.</span><span class="sxs-lookup"><span data-stu-id="13610-117">The path and name of the full replica from which to populate records.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="13610-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="13610-118">Remarks</span></span>

<span data-ttu-id="13610-119">При синхронизации частичные реплики с полной реплики, можно создать «потерянных» записей в частичные реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-119">When you synchronize a partial replica with a full replica, it is possible to create "orphaned" records in the partial replica.</span></span> <span data-ttu-id="13610-120">Допустим, у вас есть клиенты с его **[этого](tabledef-replicafilter-property-dao.md)** , задайте значение «область = «Центр сертификации»».</span><span class="sxs-lookup"><span data-stu-id="13610-120">For example, suppose you have a Customers table with its **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** set to "Region = 'CA'".</span></span> <span data-ttu-id="13610-121">При изменении пользователем региона клиента из центра сертификации для Нюнорск частичное реплики, а затем синхронизации с помощью метода **[синхронизации](database-synchronize-method-dao.md)** , изменения распределены по полной реплики, но запись, содержащую Нюнорск частичное реплики потерянные, так как теперь ИТ не соответствует условиям фильтра реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-121">If a user changes a customer's region from CA to NY in the partial replica, and then a synchronization occurs via the **[Synchronize](database-synchronize-method-dao.md)** method, the change is propagated to the full replica but the record containing NY in the partial replica is orphaned because it now doesn't meet the replica filter criteria.</span></span>

<span data-ttu-id="13610-122">Для решения проблемы потерянных записей, можно использовать метод **PopulatePartial** .</span><span class="sxs-lookup"><span data-stu-id="13610-122">To solve the problem of orphaned records, you can use the **PopulatePartial** method.</span></span> <span data-ttu-id="13610-123">Метод **PopulatePartial** похож на метод **синхронизации** , но синхронизирует все изменения с полной реплики, удаляются все записи в частичные реплики и затем повторно заполняется реплику на основе текущего фильтров реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-123">The **PopulatePartial** method is similar to the **Synchronize** method, but it synchronizes any changes with the full replica, removes all records in the partial replica, and then repopulates the partial replica based on the current replica filters.</span></span> <span data-ttu-id="13610-124">Даже в том случае, если не были изменены фильтры реплики, **PopulatePartial** всегда снимите все записи в частичные реплики и повторного наполнения его на основе текущего фильтров.</span><span class="sxs-lookup"><span data-stu-id="13610-124">Even if your replica filters have not changed, **PopulatePartial** will always clear all records in the partial replica and repopulate it based on the current filters.</span></span>

<span data-ttu-id="13610-125">Как правило следует использовать метод **PopulatePartial** при создании частичные реплики и при любом изменении фильтры реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-125">Generally, you should use the **PopulatePartial** method when you create a partial replica and whenever you change your replica filters.</span></span> <span data-ttu-id="13610-126">Если приложение изменяет реплики фильтры, необходимо выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="13610-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="13610-127">Синхронизация полной реплики с реплику, в котором изменяются фильтры.</span><span class="sxs-lookup"><span data-stu-id="13610-127">Synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="13610-128">Используйте **этого** и **[значений этих](relation-partialreplica-property-dao.md)** свойств для внесите необходимые изменения в фильтр реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-128">Use the **ReplicaFilter** and **[PartialReplica](relation-partialreplica-property-dao.md)** properties to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="13610-129">Вызовите метод **PopulatePartial** , чтобы удалить все записи из частичные реплики и перенести все записи с полной реплики, условиям фильтра новой реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-129">Call the **PopulatePartial** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="13610-130">Если вызывается метод **синхронизации** без первого вызова **PopulatePartial**фильтр реплики была изменена, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="13610-130">If a replica filter has changed, and the **Synchronize** method is invoked without first invoking **PopulatePartial**, a trappable error occurs.</span></span>

<span data-ttu-id="13610-131">Метод **PopulatePartial** может вызываться только на реплику, который был открыт для исключительного доступа.</span><span class="sxs-lookup"><span data-stu-id="13610-131">The **PopulatePartial** method can only be invoked on a partial replica that has been opened for exclusive access.</span></span> <span data-ttu-id="13610-132">Кроме того не может вызывать метод **PopulatePartial** из кода, выполняющегося в рамках реплику самого.</span><span class="sxs-lookup"><span data-stu-id="13610-132">Furthermore, you can't call the **PopulatePartial** method from code running within the partial replica itself.</span></span> <span data-ttu-id="13610-133">Вместо этого откройте реплику исключительно на основе полной реплики или другую базу данных, а затем вызывают **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="13610-133">Instead, open the partial replica exclusively from the full replica or another database, then call **PopulatePartial**.</span></span>


> [!NOTE]
> <span data-ttu-id="13610-134">Несмотря на то, что **PopulatePartial** выполняет односторонней синхронизации перед Очистка и повторного заполнения частичные реплики, рекомендуется по-прежнему вызывать **синхронизировать** до вызова метода **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="13610-134">Although **PopulatePartial** performs a one-way synchronization before clearing and repopulating the partial replica, it is still a good idea to call **Synchronize** before calling **PopulatePartial**.</span></span> <span data-ttu-id="13610-135">Это происходит в случае сбоя вызова **синхронизировать** перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="13610-135">This is because if the call to **Synchronize** fails, a trappable error occurs.</span></span> <span data-ttu-id="13610-136">Следует ли продолжить работу с помощью метода **PopulatePartial** (который удаляет все записи в частичные реплики) можно использовать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="13610-136">You can use this error to decide whether or not to proceed with the **PopulatePartial** method (which removes all records in the partial replica).</span></span> <span data-ttu-id="13610-137">Если возникает ошибка во время синхронизации записей **PopulatePartial** вызывается сам по себе, записей частичное реплики будет по-прежнему снят, могут быть результат.</span><span class="sxs-lookup"><span data-stu-id="13610-137">If **PopulatePartial** is called by itself and an error occurs while records are being synchronized, records in the partial replica will still be cleared, which may not be the desired result.</span></span>



## <a name="example"></a><span data-ttu-id="13610-138">Пример</span><span class="sxs-lookup"><span data-stu-id="13610-138">Example</span></span>

<span data-ttu-id="13610-139">В следующем примере метод **PopulatePartial** после изменения фильтра реплики.</span><span class="sxs-lookup"><span data-stu-id="13610-139">The following example uses the **PopulatePartial** method after changing a replica filter.</span></span>

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

