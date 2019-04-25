---
title: Преобразование кода DAO в ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295522"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="748b9-102">Преобразование кода DAO в ADO</span><span class="sxs-lookup"><span data-stu-id="748b9-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="748b9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="748b9-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="748b9-104">Библиотеки DAO до версии 3.6 не предоставляются и не поддерживаются в Access.</span><span class="sxs-lookup"><span data-stu-id="748b9-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="748b9-105">Сопоставление объектов DAO с ADO</span><span class="sxs-lookup"><span data-stu-id="748b9-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="748b9-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="748b9-106"><strong>VBA DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="748b9-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="748b9-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="748b9-108"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="748b9-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="748b9-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="748b9-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="748b9-110">Нет</span><span class="sxs-lookup"><span data-stu-id="748b9-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748b9-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="748b9-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="748b9-112">Нет</span><span class="sxs-lookup"><span data-stu-id="748b9-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748b9-113">Database</span><span class="sxs-lookup"><span data-stu-id="748b9-113">Database</span></span></p></td>
<td><p><span data-ttu-id="748b9-114">Connection</span><span class="sxs-lookup"><span data-stu-id="748b9-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748b9-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="748b9-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="748b9-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="748b9-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748b9-117">Тип "Динамический набор"</span><span class="sxs-lookup"><span data-stu-id="748b9-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="748b9-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="748b9-118">Keyset cursors</span></span></p></td>
<td><p><span data-ttu-id="748b9-119">Извлекает набор указателей на записи в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="748b9-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748b9-120">Тип "Статический набор"</span><span class="sxs-lookup"><span data-stu-id="748b9-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="748b9-121">Static</span><span class="sxs-lookup"><span data-stu-id="748b9-121">Static</span></span></p></td>
<td><p><span data-ttu-id="748b9-122">Оба извлекают полные записи, но набор записей Static можно обновлять.</span><span class="sxs-lookup"><span data-stu-id="748b9-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="748b9-123">Табличный тип</span><span class="sxs-lookup"><span data-stu-id="748b9-123">TableType</span></span></p></td>
<td><p><span data-ttu-id="748b9-124">Keyset с параметром adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="748b9-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="748b9-125">Field</span><span class="sxs-lookup"><span data-stu-id="748b9-125">Field</span></span></p></td>
<td><p><span data-ttu-id="748b9-126">Field</span><span class="sxs-lookup"><span data-stu-id="748b9-126">Field</span></span></p></td>
<td><p><span data-ttu-id="748b9-127">При ссылке на набор записей.</span><span class="sxs-lookup"><span data-stu-id="748b9-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="748b9-128">DAO</span><span class="sxs-lookup"><span data-stu-id="748b9-128">MFC DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="748b9-129">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="748b9-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="748b9-130">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="748b9-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="748b9-131">ADO</span><span class="sxs-lookup"><span data-stu-id="748b9-131">ADO methods</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="748b9-132">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="748b9-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="748b9-133">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="748b9-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="748b9-134">Перемещение фокуса с текущей записи с помощью методов **MoveNext, MoveLast, MoveFirst, MovePrevious** без предварительного использования метода **CancelUpdate** неявно запускает метод **Update**.</span><span class="sxs-lookup"><span data-stu-id="748b9-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="748b9-135">Об участниках</span><span class="sxs-lookup"><span data-stu-id="748b9-135">About the contributors</span></span>

<span data-ttu-id="748b9-136">**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="748b9-136">**Link provided byCommunity Member Icon** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="748b9-137">UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="748b9-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="748b9-138">Выбор между DAO и ADO</span><span class="sxs-lookup"><span data-stu-id="748b9-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

