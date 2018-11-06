---
title: Метод Database.MakeReplica (DAO)
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
ms.openlocfilehash: 45aa005b7c8337a4c5541ea7217cbdb520bb1725
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997737"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="60225-102">Метод Database.MakeReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="60225-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="60225-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60225-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60225-104">Делает новой реплики из другой реплики базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="60225-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="60225-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60225-105">Syntax</span></span>

<span data-ttu-id="60225-106">*выражение* . MakeReplica (***PathName***, ***Описание***, ***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="60225-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="60225-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="60225-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="60225-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60225-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60225-109">Имя</span><span class="sxs-lookup"><span data-stu-id="60225-109">Name</span></span></p></th>
<th><p><span data-ttu-id="60225-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="60225-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="60225-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="60225-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="60225-112">Описание</span><span class="sxs-lookup"><span data-stu-id="60225-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60225-113"><em>Имя пути</em></span><span class="sxs-lookup"><span data-stu-id="60225-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="60225-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60225-114">Required</span></span></p></td>
<td><p><span data-ttu-id="60225-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="60225-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="60225-116">Путь и имя новой реплики.</span><span class="sxs-lookup"><span data-stu-id="60225-116">The path and file name of the new replica.</span></span> <span data-ttu-id="60225-117">Если реплики существующее имя файла, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="60225-117">If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60225-118"><em>Описание</em></span><span class="sxs-lookup"><span data-stu-id="60225-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="60225-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60225-119">Required</span></span></p></td>
<td><p><span data-ttu-id="60225-120"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="60225-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="60225-121"><strong>Строка</strong> , описывающая реплики, которую вы создаете</span><span class="sxs-lookup"><span data-stu-id="60225-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60225-122"><em>Варианты</em></span><span class="sxs-lookup"><span data-stu-id="60225-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="60225-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="60225-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="60225-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="60225-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="60225-125">Константа <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> , указывающее, характеристики реплики при создании.</span><span class="sxs-lookup"><span data-stu-id="60225-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="60225-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="60225-126">Remarks</span></span>

<span data-ttu-id="60225-127">Только что созданный реплику будут иметь все **[этого](tabledef-replicafilter-property-dao.md)** свойства, значение **False**, что означает, что данные не будут в таблицах.</span><span class="sxs-lookup"><span data-stu-id="60225-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="60225-128">Пример</span><span class="sxs-lookup"><span data-stu-id="60225-128">Example</span></span>

<span data-ttu-id="60225-129">Эта функция использует метод **MakeReplica** для создания дополнительной реплики из имеющегося образца проекта.</span><span class="sxs-lookup"><span data-stu-id="60225-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="60225-130">Аргумент intOptions может быть сочетание констант **dbRepMakeReadOnly** и **dbRepMakePartial**, или она может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="60225-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="60225-131">Например, создание частичная реплика только для чтения, необходимо передать значение **dbRepMakeReadOnly** + **dbRepMakePartial** как значение intOptions.</span><span class="sxs-lookup"><span data-stu-id="60225-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

