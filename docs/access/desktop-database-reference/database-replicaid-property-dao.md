---
title: Свойство Database.ReplicaID (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3214f093b90576483df4d6f63cf1ad62b3530931
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918767"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="03eaa-102">Свойство Database.ReplicaID (DAO)</span><span class="sxs-lookup"><span data-stu-id="03eaa-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="03eaa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03eaa-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="03eaa-104">Возвращает 16-битное значение, уникальным образом идентифицирующее реплики базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="03eaa-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="03eaa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03eaa-105">Syntax</span></span>

<span data-ttu-id="03eaa-106">*выражение* . ReplicaID</span><span class="sxs-lookup"><span data-stu-id="03eaa-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="03eaa-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="03eaa-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="03eaa-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="03eaa-108">Remarks</span></span>

<span data-ttu-id="03eaa-109">Возвращаемое значение — это значение **GUID** , который уникальным образом определяет, так и основной.</span><span class="sxs-lookup"><span data-stu-id="03eaa-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="03eaa-110">Ядро базы данных Microsoft Access автоматически создает это значение при создании новой реплики.</span><span class="sxs-lookup"><span data-stu-id="03eaa-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="03eaa-111">Свойство **ReplicaID** каждой реплики (и основной) хранятся в таблице MSysReplicas системы.</span><span class="sxs-lookup"><span data-stu-id="03eaa-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="03eaa-112">Пример</span><span class="sxs-lookup"><span data-stu-id="03eaa-112">Example</span></span>

<span data-ttu-id="03eaa-113">В этом примере вносятся реплики из основной части Northwind.mdb и возвращает реплики **ReplicaID**, которая создается автоматически ядром СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="03eaa-113">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine.</span></span> <span data-ttu-id="03eaa-114">(Если основной Northwind еще не создан, ссылка на свойство **является реплицируемым** или измените имя базы данных в коде для имеющегося образца разработки).</span><span class="sxs-lookup"><span data-stu-id="03eaa-114">(If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

