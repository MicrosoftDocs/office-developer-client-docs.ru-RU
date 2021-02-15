---
title: Свойство Database.DesignMasterID (DAO)
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
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="6edb5-102">Свойство Database.DesignMasterID (DAO)</span><span class="sxs-lookup"><span data-stu-id="6edb5-102">Database.DesignMasterID property (DAO)</span></span>

<span data-ttu-id="6edb5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6edb5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6edb5-104">Задает или возвращает 16-byte-значение, которое уникальным образом идентифицирует master дизайна в наборе реплик (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6edb5-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6edb5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6edb5-105">Syntax</span></span>

<span data-ttu-id="6edb5-106">*выражение .* DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="6edb5-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="6edb5-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="6edb5-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edb5-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="6edb5-108">Remarks</span></span>

<span data-ttu-id="6edb5-109">Свойство **DesignMasterID следует** устанавливать только в том случае, если необходимо переместить текущий объект Design Master.</span><span class="sxs-lookup"><span data-stu-id="6edb5-109">You should set the **DesignMasterID** property only if you need to move the current Design Master.</span></span> <span data-ttu-id="6edb5-110">Установка этого свойства делает определенную реплику в реплике набором "Мастер проектирования".</span><span class="sxs-lookup"><span data-stu-id="6edb5-110">Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="6edb5-111">Никогда не создавайте второй мастер проектирования в наборе реплик.</span><span class="sxs-lookup"><span data-stu-id="6edb5-111">Never create a second Design Master in a replica set.</span></span> <span data-ttu-id="6edb5-112">Наличие второго мастера разработки может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="6edb5-112">The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="6edb5-113">В крайних обстоятельствах, например, если образец конструктора стирается или поврежден, можно установить это свойство в текущей реплике.</span><span class="sxs-lookup"><span data-stu-id="6edb5-113">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica.</span></span> <span data-ttu-id="6edb5-114">Однако установка этого свойства в реплике, когда в наборе уже есть другой мастер разработки, может привести к разделению реплики на два неприсоедаемых набора и предотвратить дальнейшую синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="6edb5-114">However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="6edb5-115">Если вы решили сделать реплику новым хозяином дизайна для набора, синхронизируются со всеми репликами в наборе реплик, прежде чем устанавливать свойство **DesignMasterID** в реплике.</span><span class="sxs-lookup"><span data-stu-id="6edb5-115">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica.</span></span> <span data-ttu-id="6edb5-116">Реплика должна быть открыта в монопольном режиме, чтобы сделать ее хозяином разработки.</span><span class="sxs-lookup"><span data-stu-id="6edb5-116">The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="6edb5-117">Если вы сделаете реплику, предназначенную только для чтения, в мастере разработки, целевая реплика будет выполнена для чтения и записи; Старый мастер проектирования также остается для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6edb5-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="6edb5-118">Параметр **свойства DesignMasterID** хранится в системной таблице MSysRepInfo.</span><span class="sxs-lookup"><span data-stu-id="6edb5-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="6edb5-119">Пример</span><span class="sxs-lookup"><span data-stu-id="6edb5-119">Example</span></span>

<span data-ttu-id="6edb5-120">В этом примере **свойству DesignMasterID** задан параметр **свойства ReplicaID** другой базы данных, что делает эту базу данных образцом разработки в наборе реплик.</span><span class="sxs-lookup"><span data-stu-id="6edb5-120">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set.</span></span> <span data-ttu-id="6edb5-121">Старые и новые мастера проектирования синхронизируются для обновления изменений дизайна.</span><span class="sxs-lookup"><span data-stu-id="6edb5-121">The old and new Design Masters are synchronized to update the design change.</span></span> <span data-ttu-id="6edb5-122">Чтобы этот код работал, необходимо создать мастер проектирования и реплику, включить соответствующие имена и пути, а затем запустить этот код из базы данных, которая не является старой или новой.</span><span class="sxs-lookup"><span data-stu-id="6edb5-122">For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

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

