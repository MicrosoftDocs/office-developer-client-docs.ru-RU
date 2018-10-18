---
<span data-ttu-id="fcec3-101"><<<<<<< Заголовок HEAD: преобразование кода DAO для ADO TOCTitle: преобразование кода DAO для ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 09/18/2015 === заголовок: преобразование DAO код для ADO TOCTitle: преобразование DAO кода для ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="fcec3-101"><<<<<<< HEAD title: Converting DAO Code to ADO TOCTitle: Converting DAO Code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 09/18/2015 ======= title: Convert DAO code to ADO TOCTitle: Convert DAO code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="fcec3-102">главные mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="fcec3-102">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="fcec3-103">vbaac10.chm5267115 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="fcec3-103">vbaac10.chm5267115 f1_categories:</span></span>
- <span data-ttu-id="fcec3-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="fcec3-104">Office.Version=v15</span></span>
---

<span data-ttu-id="fcec3-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fcec3-105"><<<<<<< HEAD</span></span>
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="fcec3-106">Converting DAO Code to ADO</span><span class="sxs-lookup"><span data-stu-id="fcec3-106">Converting DAO Code to ADO</span></span>
=======
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="fcec3-107">Преобразование кода DAO ADO</span><span class="sxs-lookup"><span data-stu-id="fcec3-107">Convert DAO code to ADO</span></span>
>>>>>>> <span data-ttu-id="fcec3-108">master</span><span class="sxs-lookup"><span data-stu-id="fcec3-108">master</span></span>

<span data-ttu-id="fcec3-109">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcec3-109">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="fcec3-110">Версии библиотеки DAO перед 3.6 не предоставляются и не поддерживаются в клиенте.</span><span class="sxs-lookup"><span data-stu-id="fcec3-110">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="fcec3-111">DAO карту объект ADO</span><span class="sxs-lookup"><span data-stu-id="fcec3-111">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcec3-112"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="fcec3-112"><strong>DAO</strong></span></span></p></th>
<span data-ttu-id="fcec3-113"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fcec3-113"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="fcec3-114"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="fcec3-114"><strong>ADO(ADODB)</strong></span></span></p></th>
=======
<th><p><span data-ttu-id="fcec3-115"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="fcec3-115"><strong>ADO (ADODB)</strong></span></span></p></th><span data-ttu-id="fcec3-116">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="fcec3-116">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="fcec3-117"><strong>Примечание</strong></span><span class="sxs-lookup"><span data-stu-id="fcec3-117"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcec3-118">DBEngine</span><span class="sxs-lookup"><span data-stu-id="fcec3-118">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="fcec3-119">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fcec3-119">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcec3-120">Рабочая область</span><span class="sxs-lookup"><span data-stu-id="fcec3-120">Workspace</span></span></p></td>
<td><p><span data-ttu-id="fcec3-121">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fcec3-121">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcec3-122">База данных</span><span class="sxs-lookup"><span data-stu-id="fcec3-122">Database</span></span></p></td>
<td><p><span data-ttu-id="fcec3-123">Подключение</span><span class="sxs-lookup"><span data-stu-id="fcec3-123">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcec3-124">Набор записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-124">Recordset</span></span></p></td>
<td><p><span data-ttu-id="fcec3-125">Набор записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-125">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcec3-126">Добавляющий</span><span class="sxs-lookup"><span data-stu-id="fcec3-126">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="fcec3-127">Набор ключей</span><span class="sxs-lookup"><span data-stu-id="fcec3-127">Keyset</span></span></p></td>
<span data-ttu-id="fcec3-128"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fcec3-128"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="fcec3-129">Получает набор указатели на записей в наборе</span><span class="sxs-lookup"><span data-stu-id="fcec3-129">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="fcec3-130">Извлекает набор указателей на записи в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="fcec3-130">Retrieves a set of pointers to the records in the recordset.</span></span></p></td><span data-ttu-id="fcec3-131">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="fcec3-131">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcec3-132">Тип моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="fcec3-132">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="fcec3-133">Статическое</span><span class="sxs-lookup"><span data-stu-id="fcec3-133">Static</span></span></p></td>
<span data-ttu-id="fcec3-134"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fcec3-134"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="fcec3-135">Оба Получение полного записей, но могут быть обновлены статического набора записей.</span><span class="sxs-lookup"><span data-stu-id="fcec3-135">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcec3-136">Тип таблицы</span><span class="sxs-lookup"><span data-stu-id="fcec3-136">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="fcec3-137">Набор ключей с adCmdTableDirect параметр</span><span class="sxs-lookup"><span data-stu-id="fcec3-137">Keyset with adCmdTableDirect Option</span></span></p></td>
=======
<td><p><span data-ttu-id="fcec3-138">Оба Получение полного записей, но могут быть обновлены статического набора записей.</span><span class="sxs-lookup"><span data-stu-id="fcec3-138">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcec3-139">Тип таблицы</span><span class="sxs-lookup"><span data-stu-id="fcec3-139">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="fcec3-140">Набор ключей с помощью параметра adCmdTableDirect.</span><span class="sxs-lookup"><span data-stu-id="fcec3-140">Keyset with adCmdTableDirect option.</span></span></p></td><span data-ttu-id="fcec3-141">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="fcec3-141">
>>>>>>> master</span></span>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcec3-142">Поле</span><span class="sxs-lookup"><span data-stu-id="fcec3-142">Field</span></span></p></td>
<td><p><span data-ttu-id="fcec3-143">Поле</span><span class="sxs-lookup"><span data-stu-id="fcec3-143">Field</span></span></p></td>
<span data-ttu-id="fcec3-144"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fcec3-144"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="fcec3-145">Если в наборе записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-145">When referred to in a recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="fcec3-146">Если приведенные в набор записей.</span><span class="sxs-lookup"><span data-stu-id="fcec3-146">When referred to in a recordset.</span></span></p></td><span data-ttu-id="fcec3-147">
>>>>>>>Образец</span><span class="sxs-lookup"><span data-stu-id="fcec3-147">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="fcec3-148">DAO</span><span class="sxs-lookup"><span data-stu-id="fcec3-148">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="fcec3-149">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-149">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="fcec3-150">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-150">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="fcec3-151">ADO</span><span class="sxs-lookup"><span data-stu-id="fcec3-151">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="fcec3-152">Открытие набора записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-152">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="fcec3-153">Изменение набора записей</span><span class="sxs-lookup"><span data-stu-id="fcec3-153">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
<span data-ttu-id="fcec3-154"><<<<<<< Перемещение HEAD фокус из текущей записи с помощью **MoveNext MoveLast MoveFirst MovePrevious** без сначала с помощью метода **CancelUpdate** неявного выполнения метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="fcec3-154"><<<<<<< HEAD Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>
> <span data-ttu-id="fcec3-155">=== Перемещения фокуса от текущей записи через **MoveNext, MoveLast, MoveFirst, MovePrevious** без использования метода **CancelUpdate** неявно выполняет метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="fcec3-155">======= Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>
>>>>>>> <span data-ttu-id="fcec3-156">master</span><span class="sxs-lookup"><span data-stu-id="fcec3-156">master</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="fcec3-157">О участники</span><span class="sxs-lookup"><span data-stu-id="fcec3-157">About the contributors</span></span>

<span data-ttu-id="fcec3-158">**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="fcec3-158">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="fcec3-159">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fcec3-159">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="fcec3-160">Выбор между DAO и ADO</span><span class="sxs-lookup"><span data-stu-id="fcec3-160">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<span data-ttu-id="fcec3-161"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="fcec3-161"><<<<<<< HEAD</span></span>

=======
<br/>
>>>>>>> <span data-ttu-id="fcec3-162">master</span><span class="sxs-lookup"><span data-stu-id="fcec3-162">master</span></span>

