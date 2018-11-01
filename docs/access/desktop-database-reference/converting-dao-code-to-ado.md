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
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876745"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="4b957-102">Преобразование кода DAO в ADO</span><span class="sxs-lookup"><span data-stu-id="4b957-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="4b957-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b957-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="4b957-104">Версии библиотеки DAO перед 3.6 не предоставляются и не поддерживаются в клиенте.</span><span class="sxs-lookup"><span data-stu-id="4b957-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="4b957-105">DAO карту объект ADO</span><span class="sxs-lookup"><span data-stu-id="4b957-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b957-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="4b957-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="4b957-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="4b957-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="4b957-108"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="4b957-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b957-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="4b957-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="4b957-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4b957-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b957-111">Рабочая область</span><span class="sxs-lookup"><span data-stu-id="4b957-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="4b957-112">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4b957-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b957-113">База данных</span><span class="sxs-lookup"><span data-stu-id="4b957-113">Database</span></span></p></td>
<td><p><span data-ttu-id="4b957-114">Подключение</span><span class="sxs-lookup"><span data-stu-id="4b957-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b957-115">Набор записей</span><span class="sxs-lookup"><span data-stu-id="4b957-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="4b957-116">Набор записей</span><span class="sxs-lookup"><span data-stu-id="4b957-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b957-117">Добавляющий</span><span class="sxs-lookup"><span data-stu-id="4b957-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="4b957-118">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="4b957-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="4b957-119">Извлекает набор указателей на записи в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="4b957-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b957-120">Тип моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="4b957-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="4b957-121">Статическое</span><span class="sxs-lookup"><span data-stu-id="4b957-121">Static</span></span></p></td>
<td><p><span data-ttu-id="4b957-122">Оба Получение полного записей, но могут быть обновлены статического набора записей.</span><span class="sxs-lookup"><span data-stu-id="4b957-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b957-123">Тип таблицы</span><span class="sxs-lookup"><span data-stu-id="4b957-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="4b957-124">Набор ключей с помощью параметра adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="4b957-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b957-125">Поле</span><span class="sxs-lookup"><span data-stu-id="4b957-125">Field</span></span></p></td>
<td><p><span data-ttu-id="4b957-126">Поле</span><span class="sxs-lookup"><span data-stu-id="4b957-126">Field</span></span></p></td>
<td><p><span data-ttu-id="4b957-127">Если приведенные в набор записей.</span><span class="sxs-lookup"><span data-stu-id="4b957-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="4b957-128">DAO</span><span class="sxs-lookup"><span data-stu-id="4b957-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="4b957-129">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="4b957-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="4b957-130">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="4b957-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="4b957-131">ADO</span><span class="sxs-lookup"><span data-stu-id="4b957-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="4b957-132">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="4b957-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="4b957-133">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="4b957-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="4b957-134">Перемещение фокуса из текущей записи через **MoveNext, MoveLast, MoveFirst, MovePrevious** без использования метода **CancelUpdate** неявно выполняет метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="4b957-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="4b957-135">О участники</span><span class="sxs-lookup"><span data-stu-id="4b957-135">About the contributors</span></span>

<span data-ttu-id="4b957-136">**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="4b957-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="4b957-137">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4b957-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="4b957-138">Выбор между DAO и ADO</span><span class="sxs-lookup"><span data-stu-id="4b957-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

