---
title: Метод Connection. Execute (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295914"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="e6647-102">Метод Connection. Execute (DAO)</span><span class="sxs-lookup"><span data-stu-id="e6647-102">Connection.Execute method (DAO)</span></span>

<span data-ttu-id="e6647-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6647-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6647-104">Выполняет запрос на изменение или выполняет инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="e6647-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6647-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6647-105">Syntax</span></span>

<span data-ttu-id="e6647-106">*Expression* . Выполнение (***запрос***, ***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="e6647-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="e6647-107">*Expression (выражение* ) Переменная, представляющая объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="e6647-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6647-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6647-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6647-109">Имя</span><span class="sxs-lookup"><span data-stu-id="e6647-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e6647-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="e6647-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e6647-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e6647-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e6647-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e6647-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6647-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="e6647-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="e6647-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e6647-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e6647-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-116"><strong>Строка</strong> , которая является оператором SQL или значением свойства <strong>имени</strong> объекта <strong>QueryDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="e6647-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6647-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="e6647-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="e6647-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="e6647-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="e6647-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-120">Константа или сочетание констант, определяющих характеристики целостности данных запроса, как указано в параметрах.</span><span class="sxs-lookup"><span data-stu-id="e6647-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e6647-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="e6647-121">Remarks</span></span>

<span data-ttu-id="e6647-122">Для параметров можно использовать следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="e6647-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6647-123">Константа</span><span class="sxs-lookup"><span data-stu-id="e6647-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="e6647-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e6647-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6647-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-126">Запрещает разрешение на запись для других пользователей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6647-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6647-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-128">Умолчани Выполняет несогласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6647-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6647-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-130">Выполняет согласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6647-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6647-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-132">Выполняет запрос к серверу SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e6647-132">Executes an SQL pass-through query.</span></span> <span data-ttu-id="e6647-133">При установке этого параметра инструкция SQL передается в базу данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6647-133">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6647-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-135">Откат обновлений при возникновении ошибки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6647-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6647-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-137">Создает ошибку во время выполнения, если другой пользователь изменяет редактируемые данные (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6647-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6647-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-139">Асинхронно выполняет запрос (только объекты подключения ODBCDirect и объекты QueryDef).</span><span class="sxs-lookup"><span data-stu-id="e6647-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6647-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="e6647-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="e6647-141">Выполняет оператор без первого вызова функции API ODBC Склпрепаре (только для соединений и объектов QueryDef).</span><span class="sxs-lookup"><span data-stu-id="e6647-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e6647-142">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e6647-142">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e6647-143">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e6647-143">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="e6647-144">Константы **дбконсистент** и **дбинконсистент** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e6647-144">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive.</span></span> <span data-ttu-id="e6647-145">Можно использовать один или другой, но не то и другое в данном экземпляре **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="e6647-145">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="e6647-146">Использование как **дбконсистент** , так и **дбинконсистент** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e6647-146">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="e6647-147">Метод **EXECUTE** действителен только для запросов на изменение.</span><span class="sxs-lookup"><span data-stu-id="e6647-147">The **Execute** method is valid only for action queries.</span></span> <span data-ttu-id="e6647-148">Если вы используете **EXECUTE** с другим типом запроса, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="e6647-148">If you use **Execute** with another type of query, an error occurs.</span></span> <span data-ttu-id="e6647-149">Так как запрос на изменение не возвращает какие-либо записи, **выполнение** не возвращает **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="e6647-149">Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**.</span></span> <span data-ttu-id="e6647-150">(При выполнении запроса к серверу SQL в рабочей области ODBCDirect не возвращается сообщение об ошибке, если **набор записей** не возвращается.)</span><span class="sxs-lookup"><span data-stu-id="e6647-150">(Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="e6647-151">Используйте свойство **рекордсаффектед** объекта **Connection**, **Database**или **QueryDef** , чтобы определить количество записей, затронутых последним методом **EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="e6647-151">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method.</span></span> <span data-ttu-id="e6647-152">Например, **рекордсаффектед** содержит число записей, удаленных, обновленных или вставленных при выполнении запроса на изменение.</span><span class="sxs-lookup"><span data-stu-id="e6647-152">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="e6647-153">При использовании метода **EXECUTE** для запуска запроса свойство **рекордсаффектед** объекта **QueryDef** устанавливается равным количеству затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="e6647-153">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="e6647-154">В рабочей области Microsoft Access, если вы задаете синтаксическую правильную инструкцию SQL и обладаете соответствующими разрешениями, метод **EXECUTE** не будет выполняться, даже если не удается изменить или удалить одну строку.</span><span class="sxs-lookup"><span data-stu-id="e6647-154">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="e6647-155">Поэтому всегда используйте параметр **дбфаилонеррор** при использовании метода **EXECUTE** для выполнения запроса на обновление или удаление.</span><span class="sxs-lookup"><span data-stu-id="e6647-155">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="e6647-156">Этот параметр создает ошибку времени выполнения и выполняет откат всех успешных изменений, если какие затронутые записи заблокированы и не могут быть обновлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="e6647-156">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="e6647-157">В более ранних версиях ядра базы данных Microsoft Jet инструкции SQL были автоматически внедрены в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="e6647-157">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="e6647-158">Если часть оператора, выполняемого с помощью **дбфаилонеррор** , завершилась с ошибкой, будет выполнен откат всего оператора.</span><span class="sxs-lookup"><span data-stu-id="e6647-158">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="e6647-159">Для повышения производительности эти неявные транзакции были удалены начиная с версии 3,5.</span><span class="sxs-lookup"><span data-stu-id="e6647-159">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="e6647-160">Если вы обновляете старые коды DAO, не забудьте использовать явные транзакции для операторов **EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="e6647-160">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="e6647-161">Для лучшей производительности в рабочей области Microsoft Access, особенно в многопользовательской среде, вложите метод **EXECUTE** в транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e6647-161">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="e6647-162">Используйте метод **BeginTrans** для текущего объекта **Workspace** , затем используйте метод **EXECUTE** и завершите транзакцию с помощью метода **CommitTrans** в **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="e6647-162">Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**.</span></span> <span data-ttu-id="e6647-163">Это сохраняет изменения на диске и освобождает все блокировки, включенные во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="e6647-163">This saves changes on disk and frees any locks placed while the query is running.</span></span>

