---
title: Свойство Database. ReplicaID (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294717"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="47c9e-102">Свойство Database. ReplicaID (DAO)</span><span class="sxs-lookup"><span data-stu-id="47c9e-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="47c9e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47c9e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="47c9e-104">Возвращает 16-байтовое значение, уникально идентифицирующее реплику базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="47c9e-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="47c9e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47c9e-105">Syntax</span></span>

<span data-ttu-id="47c9e-106">*Expression* . Одинаковые</span><span class="sxs-lookup"><span data-stu-id="47c9e-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="47c9e-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="47c9e-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c9e-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="47c9e-108">Remarks</span></span>

<span data-ttu-id="47c9e-109">Возвращаемое значение — это значение **GUID** , которое уникально идентифицирует реплику или основную реплику.</span><span class="sxs-lookup"><span data-stu-id="47c9e-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="47c9e-110">Ядро СУБД Microsoft Access автоматически создает это значение при создании новой реплики.</span><span class="sxs-lookup"><span data-stu-id="47c9e-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="47c9e-111">Свойство **replicaId** каждой реплики (и основной реплики) хранится в системной таблице мсисрепликас.</span><span class="sxs-lookup"><span data-stu-id="47c9e-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="47c9e-112">Пример</span><span class="sxs-lookup"><span data-stu-id="47c9e-112">Example</span></span>

<span data-ttu-id="47c9e-113">В этом примере создается реплика из основной реплики базы данных Northwind. mdb, а затем возвращается значение **replicaId**реплики, которое автоматически создается ядром СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="47c9e-113">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine.</span></span> <span data-ttu-id="47c9e-114">(Если вы еще не создали основную реплику базы данных, обратитесь к свойству **Реплицируемое** или измените имя базы данных в коде на существующую основную реплику.)</span><span class="sxs-lookup"><span data-stu-id="47c9e-114">(If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

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

