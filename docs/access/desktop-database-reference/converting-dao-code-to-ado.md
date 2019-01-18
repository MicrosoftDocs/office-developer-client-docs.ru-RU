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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720340"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="db367-102">Преобразование кода DAO в ADO</span><span class="sxs-lookup"><span data-stu-id="db367-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="db367-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db367-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="db367-104">Версии библиотеки DAO перед 3.6 не предоставляются и не поддерживаются в клиенте.</span><span class="sxs-lookup"><span data-stu-id="db367-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="db367-105">DAO карту объект ADO</span><span class="sxs-lookup"><span data-stu-id="db367-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db367-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="db367-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="db367-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="db367-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="db367-108"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="db367-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db367-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="db367-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="db367-110">Нет</span><span class="sxs-lookup"><span data-stu-id="db367-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db367-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="db367-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="db367-112">Нет</span><span class="sxs-lookup"><span data-stu-id="db367-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db367-113">База данных</span><span class="sxs-lookup"><span data-stu-id="db367-113">Database</span></span></p></td>
<td><p><span data-ttu-id="db367-114">Connection</span><span class="sxs-lookup"><span data-stu-id="db367-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db367-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="db367-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="db367-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="db367-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db367-117">Добавляющий</span><span class="sxs-lookup"><span data-stu-id="db367-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="db367-118">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="db367-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="db367-119">Извлекает набор указателей на записи в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="db367-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db367-120">Тип моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="db367-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="db367-121">Статическое</span><span class="sxs-lookup"><span data-stu-id="db367-121">Static</span></span></p></td>
<td><p><span data-ttu-id="db367-122">Оба Получение полного записей, но могут быть обновлены статического набора записей.</span><span class="sxs-lookup"><span data-stu-id="db367-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db367-123">Тип таблицы</span><span class="sxs-lookup"><span data-stu-id="db367-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="db367-124">Набор ключей с помощью параметра adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="db367-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db367-125">Поле</span><span class="sxs-lookup"><span data-stu-id="db367-125">Field</span></span></p></td>
<td><p><span data-ttu-id="db367-126">Поле</span><span class="sxs-lookup"><span data-stu-id="db367-126">Field</span></span></p></td>
<td><p><span data-ttu-id="db367-127">Если приведенные в набор записей.</span><span class="sxs-lookup"><span data-stu-id="db367-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="db367-128">DAO</span><span class="sxs-lookup"><span data-stu-id="db367-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="db367-129">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="db367-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="db367-130">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="db367-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="db367-131">ADO</span><span class="sxs-lookup"><span data-stu-id="db367-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="db367-132">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="db367-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="db367-133">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="db367-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="db367-134">Перемещение фокуса из текущей записи через **MoveNext, MoveLast, MoveFirst, MovePrevious** без использования метода **CancelUpdate** неявно выполняет метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="db367-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="db367-135">О участники</span><span class="sxs-lookup"><span data-stu-id="db367-135">About the contributors</span></span>

<span data-ttu-id="db367-136">**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="db367-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="db367-137">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="db367-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="db367-138">Выбор между DAO и ADO</span><span class="sxs-lookup"><span data-stu-id="db367-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

