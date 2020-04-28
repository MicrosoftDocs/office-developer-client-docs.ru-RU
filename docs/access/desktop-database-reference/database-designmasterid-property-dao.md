---
title: Свойство Database. Десигнмастерид (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a189d16880fccdc34c169aee61c6781e1d86afa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294934"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="7afdd-102">Свойство Database. Десигнмастерид (DAO)</span><span class="sxs-lookup"><span data-stu-id="7afdd-102">Database.DesignMasterID property (DAO)</span></span>

<span data-ttu-id="7afdd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7afdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7afdd-104">Задает или возвращает 16-байтовое значение, которое уникально определяет основную реплику в наборе реплик (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7afdd-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7afdd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7afdd-105">Syntax</span></span>

<span data-ttu-id="7afdd-106">*Expression* . десигнмастерид</span><span class="sxs-lookup"><span data-stu-id="7afdd-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="7afdd-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="7afdd-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7afdd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="7afdd-108">Remarks</span></span>

<span data-ttu-id="7afdd-109">Свойство **десигнмастерид** следует задавать только в том случае, если требуется переместить текущую основную реплику.</span><span class="sxs-lookup"><span data-stu-id="7afdd-109">You should set the **DesignMasterID** property only if you need to move the current Design Master.</span></span> <span data-ttu-id="7afdd-110">При установке этого свойства в реплике устанавливается основная реплика.</span><span class="sxs-lookup"><span data-stu-id="7afdd-110">Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="7afdd-111">Никогда не создавайте вторую основную реплику в наборе реплик.</span><span class="sxs-lookup"><span data-stu-id="7afdd-111">Never create a second Design Master in a replica set.</span></span> <span data-ttu-id="7afdd-112">Наличие второй основной реплики может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="7afdd-112">The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="7afdd-113">В экстремальных обстоятельствах — например, если основная реплика удаляется или повреждается, можно задать это свойство в текущей реплике.</span><span class="sxs-lookup"><span data-stu-id="7afdd-113">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica.</span></span> <span data-ttu-id="7afdd-114">Тем не менее, задание этого свойства в реплике при наличии другой основной реплики в наборе может разделить набор реплик на два набора ирреконЦилабле и предотвратить дальнейшую синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="7afdd-114">However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="7afdd-115">Если вы решили сделать реплику новой основной репликой для набора, синхронизируйте ее со всеми репликами в наборе реплик, прежде чем устанавливать свойство **десигнмастерид** в реплике.</span><span class="sxs-lookup"><span data-stu-id="7afdd-115">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica.</span></span> <span data-ttu-id="7afdd-116">Реплика должна быть открыта в монопольном режиме, чтобы сделать ее основной.</span><span class="sxs-lookup"><span data-stu-id="7afdd-116">The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="7afdd-117">Если вы сделаете реплику, предназначенную только для чтения, в основной реплике, Целевая реплика становится доступна для чтения и записи; Старая основная реплика также остается для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7afdd-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="7afdd-118">Значение свойства **десигнмастерид** хранится в системной таблице мсисрепинфо.</span><span class="sxs-lookup"><span data-stu-id="7afdd-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="7afdd-119">Пример</span><span class="sxs-lookup"><span data-stu-id="7afdd-119">Example</span></span>

<span data-ttu-id="7afdd-120">В этом примере показано, как задать для свойства **десигнмастерид** значение свойства **replicaId** другой базы данных, сделав эту базу данных основной репликой в наборе реплик.</span><span class="sxs-lookup"><span data-stu-id="7afdd-120">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set.</span></span> <span data-ttu-id="7afdd-121">Старые и новые шаблоны оформления синхронизируются, чтобы обновить изменения структуры.</span><span class="sxs-lookup"><span data-stu-id="7afdd-121">The old and new Design Masters are synchronized to update the design change.</span></span> <span data-ttu-id="7afdd-122">Чтобы этот код работал, необходимо создать основную реплику и реплику, включить их имена и пути, а затем запустить этот код из базы данных, отличной от старой или новой основной реплики.</span><span class="sxs-lookup"><span data-stu-id="7afdd-122">For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

