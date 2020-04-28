---
title: Метод Database. Макереплика (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294920"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="6c42b-102">Метод Database. Макереплика (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c42b-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="6c42b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c42b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c42b-104">Создает новую реплику из другой реплики базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6c42b-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c42b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c42b-105">Syntax</span></span>

<span data-ttu-id="6c42b-106">*Expression* . Макереплика (***путь***, ***Описание***, ***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="6c42b-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="6c42b-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="6c42b-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c42b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c42b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c42b-109">Имя</span><span class="sxs-lookup"><span data-stu-id="6c42b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6c42b-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="6c42b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6c42b-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6c42b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6c42b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6c42b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c42b-113"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="6c42b-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="6c42b-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6c42b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6c42b-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6c42b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6c42b-116">Путь и имя файла новой реплики.</span><span class="sxs-lookup"><span data-stu-id="6c42b-116">The path and file name of the new replica.</span></span> <span data-ttu-id="6c42b-117">Если реплика является именем существующего файла, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="6c42b-117">If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c42b-118"><em>Description</em></span><span class="sxs-lookup"><span data-stu-id="6c42b-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="6c42b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6c42b-119">Required</span></span></p></td>
<td><p><span data-ttu-id="6c42b-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6c42b-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6c42b-121"><strong>Строка</strong> , описывающая создаваемую реплику</span><span class="sxs-lookup"><span data-stu-id="6c42b-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c42b-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="6c42b-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="6c42b-123">Необязательно</span><span class="sxs-lookup"><span data-stu-id="6c42b-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="6c42b-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6c42b-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6c42b-125">Константа <strong><a href="replicatypeenum-enumeration-dao.md">репликатипинум</a></strong> , определяющая характеристики создаваемой реплики.</span><span class="sxs-lookup"><span data-stu-id="6c42b-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6c42b-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c42b-126">Remarks</span></span>

<span data-ttu-id="6c42b-127">Только что созданная частичная реплика будет иметь все свойства **[репликафилтер](tabledef-replicafilter-property-dao.md)** со значением **false**, что означает, что в таблицах не будет данных.</span><span class="sxs-lookup"><span data-stu-id="6c42b-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="6c42b-128">Пример</span><span class="sxs-lookup"><span data-stu-id="6c42b-128">Example</span></span>

<span data-ttu-id="6c42b-129">Эта функция использует метод **макереплика** для создания дополнительной реплики существующей основной реплики.</span><span class="sxs-lookup"><span data-stu-id="6c42b-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="6c42b-130">Аргумент Интоптионс может быть сочетанием констант **дбрепмакереадонли** и **дбрепмакепартиал**, а также может быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="6c42b-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="6c42b-131">Например, чтобы создать частичную реплику только для чтения, необходимо передать значение **дбрепмакереадонли** + **дбрепмакепартиал** в качестве значения интоптионс.</span><span class="sxs-lookup"><span data-stu-id="6c42b-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

