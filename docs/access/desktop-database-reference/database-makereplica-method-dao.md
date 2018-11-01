---
title: Database.MakeReplica Method (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c8274d441c246d7363ec5d5c603c3079da732c84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880805"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="46a4d-102">Database.MakeReplica Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="46a4d-102">Database.MakeReplica Method (DAO)</span></span>

<span data-ttu-id="46a4d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46a4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46a4d-104">Делает новой реплики из другой реплики базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="46a4d-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="46a4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46a4d-105">Syntax</span></span>

<span data-ttu-id="46a4d-106">*выражение* . MakeReplica (***PathName***, ***Описание***, ***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="46a4d-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="46a4d-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="46a4d-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="46a4d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46a4d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46a4d-109">Имя</span><span class="sxs-lookup"><span data-stu-id="46a4d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="46a4d-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="46a4d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="46a4d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="46a4d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="46a4d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="46a4d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46a4d-113">Имя пути</span><span class="sxs-lookup"><span data-stu-id="46a4d-113">PathName</span></span></p></td>
<td><p><span data-ttu-id="46a4d-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46a4d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="46a4d-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="46a4d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="46a4d-116">Путь и имя новой реплики.</span><span class="sxs-lookup"><span data-stu-id="46a4d-116">The path and file name of the new replica.</span></span> <span data-ttu-id="46a4d-117">Если реплики существующее имя файла, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="46a4d-117">If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46a4d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="46a4d-118">Description</span></span></p></td>
<td><p><span data-ttu-id="46a4d-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46a4d-119">Required</span></span></p></td>
<td><p><span data-ttu-id="46a4d-120"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="46a4d-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="46a4d-121"><strong>Строка</strong> , описывающая реплики, которую вы создаете</span><span class="sxs-lookup"><span data-stu-id="46a4d-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46a4d-122">Options</span><span class="sxs-lookup"><span data-stu-id="46a4d-122">Options</span></span></p></td>
<td><p><span data-ttu-id="46a4d-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="46a4d-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="46a4d-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="46a4d-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="46a4d-125">Константа <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> , указывающее, характеристики реплики при создании.</span><span class="sxs-lookup"><span data-stu-id="46a4d-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="46a4d-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="46a4d-126">Remarks</span></span>

<span data-ttu-id="46a4d-127">Только что созданный реплику будут иметь все **[этого](tabledef-replicafilter-property-dao.md)** свойства, значение **False**, что означает, что данные не будут в таблицах.</span><span class="sxs-lookup"><span data-stu-id="46a4d-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="46a4d-128">Пример</span><span class="sxs-lookup"><span data-stu-id="46a4d-128">Example</span></span>

<span data-ttu-id="46a4d-129">Эта функция использует метод **MakeReplica** для создания дополнительной реплики из имеющегося образца проекта.</span><span class="sxs-lookup"><span data-stu-id="46a4d-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="46a4d-130">Аргумент intOptions может быть сочетание констант **dbRepMakeReadOnly** и **dbRepMakePartial**, или она может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="46a4d-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="46a4d-131">Например, создание частичная реплика только для чтения, необходимо передать значение **dbRepMakeReadOnly** + **dbRepMakePartial** как значение intOptions.</span><span class="sxs-lookup"><span data-stu-id="46a4d-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

