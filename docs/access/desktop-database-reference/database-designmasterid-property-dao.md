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
ms.openlocfilehash: 1d15cc036b33e2b64f54b89f4f8ed5c69d9fdcbe
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930492"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="a7305-102">Свойство Database.DesignMasterID (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7305-102">Database.DesignMasterID property (DAO)</span></span>

<span data-ttu-id="a7305-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7305-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7305-104">Задает или возвращает 16-битное значение, уникальным образом идентифицирующее репликой в наборе реплик (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a7305-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7305-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7305-105">Syntax</span></span>

<span data-ttu-id="a7305-106">*выражение* . DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="a7305-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="a7305-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="a7305-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7305-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7305-108">Remarks</span></span>

<span data-ttu-id="a7305-109">Свойство **DesignMasterID** следует устанавливать только в том случае, если необходимо перенести текущей основной.</span><span class="sxs-lookup"><span data-stu-id="a7305-109">You should set the **DesignMasterID** property only if you need to move the current Design Master.</span></span> <span data-ttu-id="a7305-110">Установка для этого свойства выполняет определенные в реплике набора реплик основной.</span><span class="sxs-lookup"><span data-stu-id="a7305-110">Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="a7305-111">Никогда не создавать второй репликой в наборе реплик.</span><span class="sxs-lookup"><span data-stu-id="a7305-111">Never create a second Design Master in a replica set.</span></span> <span data-ttu-id="a7305-112">Наличие из второго основной реплике может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="a7305-112">The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="a7305-113">Чрезмерную обстоятельствах — например, если основной удалены или повреждены — это свойство можно задать в текущей реплики.</span><span class="sxs-lookup"><span data-stu-id="a7305-113">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica.</span></span> <span data-ttu-id="a7305-114">Тем не менее Установка этого свойства реплики при наборе уже существует другой реплике может разделы наборе на два набора несовместимые и предотвратить дальнейшая синхронизация данных.</span><span class="sxs-lookup"><span data-stu-id="a7305-114">However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="a7305-115">Если вы решили создать новый основной набор реплику, синхронизируйте его с все реплики в наборе перед установкой **DesignMasterID** в реплике репликации.</span><span class="sxs-lookup"><span data-stu-id="a7305-115">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica.</span></span> <span data-ttu-id="a7305-116">Чтобы сделать его основной реплики необходимо открыть в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="a7305-116">The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="a7305-117">При внесении реплики, предназначенная только для чтения в основной, реплики конечного выполняется чтение и запись; старый основной также остается чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a7305-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="a7305-118">Настройка свойства **DesignMasterID** хранится в таблице MSysRepInfo системы.</span><span class="sxs-lookup"><span data-stu-id="a7305-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="a7305-119">Пример</span><span class="sxs-lookup"><span data-stu-id="a7305-119">Example</span></span>

<span data-ttu-id="a7305-120">В этом примере присваивает свойству **DesignMasterID** значение свойства **ReplicaID** Установка другой базы данных, что делает репликой в наборе реплик базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7305-120">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set.</span></span> <span data-ttu-id="a7305-121">Образцы оформления старой и новой синхронизированы для обновления изменения.</span><span class="sxs-lookup"><span data-stu-id="a7305-121">The old and new Design Masters are synchronized to update the design change.</span></span> <span data-ttu-id="a7305-122">Для работы этого кода необходимо создать основной реплики и реплики, включают их имена и пути к соответствующим образом и запуска этого кода из отличный от старой и новой основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7305-122">For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

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

