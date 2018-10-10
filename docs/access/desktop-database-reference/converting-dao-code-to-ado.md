---
title: Converting DAO Code to ADO
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479780"
---
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="fc7d1-102">Converting DAO Code to ADO</span><span class="sxs-lookup"><span data-stu-id="fc7d1-102">Converting DAO Code to ADO</span></span>

<span data-ttu-id="fc7d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc7d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="fc7d1-104">Версии библиотеки DAO перед 3.6 не предоставляются и не поддерживаются в клиенте.</span><span class="sxs-lookup"><span data-stu-id="fc7d1-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="fc7d1-105">DAO карту объект ADO</span><span class="sxs-lookup"><span data-stu-id="fc7d1-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc7d1-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="fc7d1-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="fc7d1-107"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="fc7d1-107"><strong>ADO(ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="fc7d1-108"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="fc7d1-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc7d1-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="fc7d1-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fc7d1-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7d1-111">Рабочая область</span><span class="sxs-lookup"><span data-stu-id="fc7d1-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-112">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fc7d1-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc7d1-113">База данных</span><span class="sxs-lookup"><span data-stu-id="fc7d1-113">Database</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-114">Подключение</span><span class="sxs-lookup"><span data-stu-id="fc7d1-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7d1-115">Набор записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-116">Набор записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc7d1-117">Добавляющий</span><span class="sxs-lookup"><span data-stu-id="fc7d1-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-118">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-119">Получает набор указатели на записей в наборе</span><span class="sxs-lookup"><span data-stu-id="fc7d1-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7d1-120">Тип моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="fc7d1-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-121">Статическое</span><span class="sxs-lookup"><span data-stu-id="fc7d1-121">Static</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-122">Оба Получение полного записей, но могут быть обновлены статического набора записей.</span><span class="sxs-lookup"><span data-stu-id="fc7d1-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc7d1-123">Тип таблицы</span><span class="sxs-lookup"><span data-stu-id="fc7d1-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-124">Набор ключей с adCmdTableDirect параметр</span><span class="sxs-lookup"><span data-stu-id="fc7d1-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc7d1-125">Поле</span><span class="sxs-lookup"><span data-stu-id="fc7d1-125">Field</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-126">Поле</span><span class="sxs-lookup"><span data-stu-id="fc7d1-126">Field</span></span></p></td>
<td><p><span data-ttu-id="fc7d1-127">Если в наборе записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="fc7d1-128">DAO</span><span class="sxs-lookup"><span data-stu-id="fc7d1-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="fc7d1-129">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="fc7d1-130">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="fc7d1-131">ADO</span><span class="sxs-lookup"><span data-stu-id="fc7d1-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="fc7d1-132">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="fc7d1-133">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="fc7d1-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="fc7d1-134">Перемещение фокуса из текущей записи через **MoveNext, MoveLast, MoveFirst, MovePrevious** без использования метода **CancelUpdate** неявного выполнения метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="fc7d1-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="fc7d1-135">О участники</span><span class="sxs-lookup"><span data-stu-id="fc7d1-135">About the contributors</span></span>

<span data-ttu-id="fc7d1-136">**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="fc7d1-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="fc7d1-137">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fc7d1-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="fc7d1-138">Выбор между DAO и ADO</span><span class="sxs-lookup"><span data-stu-id="fc7d1-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



