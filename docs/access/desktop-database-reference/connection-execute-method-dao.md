---
title: Connection.Exeметод (DAO)
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
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="d2c11-102">Connection.Exeметод (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2c11-102">Connection.Execute method (DAO)</span></span>

<span data-ttu-id="d2c11-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2c11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2c11-104">Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2c11-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c11-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2c11-105">Syntax</span></span>

<span data-ttu-id="d2c11-106">*выражение* .Execute(***Query***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="d2c11-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="d2c11-107">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="d2c11-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2c11-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2c11-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2c11-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d2c11-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d2c11-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="d2c11-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d2c11-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d2c11-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d2c11-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d2c11-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2c11-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="d2c11-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="d2c11-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d2c11-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d2c11-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-116"><strong>Строка,</strong> которая является SQL или <strong>свойством Name</strong> объекта <strong>QueryDef.</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c11-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="d2c11-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="d2c11-118">Необязательно</span><span class="sxs-lookup"><span data-stu-id="d2c11-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="d2c11-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-120">Константа или сочетание констант, определяющий характеристики целостности данных запроса, как указано в Параметры.</span><span class="sxs-lookup"><span data-stu-id="d2c11-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d2c11-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2c11-121">Remarks</span></span>

<span data-ttu-id="d2c11-122">Можно использовать следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** для параметров.</span><span class="sxs-lookup"><span data-stu-id="d2c11-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d2c11-123">Константа</span><span class="sxs-lookup"><span data-stu-id="d2c11-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="d2c11-124">Описание</span><span class="sxs-lookup"><span data-stu-id="d2c11-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d2c11-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-126">Отказывает в разрешении на запись другим пользователям (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d2c11-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c11-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-128">(По умолчанию) Выполняет несогласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d2c11-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c11-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-130">Выполняет согласованные обновления (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d2c11-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c11-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-132">Выполняет SQL-запрос к серверу.</span><span class="sxs-lookup"><span data-stu-id="d2c11-132">Executes an SQL pass-through query.</span></span> <span data-ttu-id="d2c11-133">При установке этого параметра инструкция SQL передается в базу данных ODBC для обработки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d2c11-133">Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c11-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-135">Выполняет откат обновлений, если возникает ошибка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d2c11-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c11-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-137">Создает ошибку во время выполнения, если другой пользователь пытается изменить данные, которые вы редактируете (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d2c11-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d2c11-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-139">Выполняет запрос асинхронно (только для объектов ODBCDirect Connection и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="d2c11-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d2c11-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="d2c11-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="d2c11-141">Выполняет инструкцию, не вызывая перед этим функцию API ODBC SQLPrepare (только для объектов ODBCDirect Connection и QueryDef).</span><span class="sxs-lookup"><span data-stu-id="d2c11-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d2c11-142">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="d2c11-142">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="d2c11-143">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d2c11-143">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="d2c11-144">Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="d2c11-144">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive.</span></span> <span data-ttu-id="d2c11-145">В том или ином экземпляре **OpenRecordset** можно использовать любую из них, но не обе.</span><span class="sxs-lookup"><span data-stu-id="d2c11-145">You can use one or the other, but not both in a given instance of **OpenRecordset**.</span></span> <span data-ttu-id="d2c11-146">Одновременное использование **dbConsistent** и **dbInconsistent** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d2c11-146">Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="d2c11-147">Метод **Execute** допустим только для запросов на изменение.</span><span class="sxs-lookup"><span data-stu-id="d2c11-147">The **Execute** method is valid only for action queries.</span></span> <span data-ttu-id="d2c11-148">Если вы используете метод **Execute** с другим типом запроса, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="d2c11-148">If you use **Execute** with another type of query, an error occurs.</span></span> <span data-ttu-id="d2c11-149">Так как запрос на изменение не возвращает записи, метод **Execute** не возвращает объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d2c11-149">Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**.</span></span> <span data-ttu-id="d2c11-150">(Выполнение запроса SQL к серверу в рабочей области ODBCDirect не вызывает ошибку, если не возвращается объект **Recordset**.)</span><span class="sxs-lookup"><span data-stu-id="d2c11-150">(Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="d2c11-151">Свойство **RecordsAffected** объекта **Connection**, **Database** или **QueryDef** используется для определения числа записей, затронутых самым последним вызовом метода **Execute**.</span><span class="sxs-lookup"><span data-stu-id="d2c11-151">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method.</span></span> <span data-ttu-id="d2c11-152">Например, **RecordsAffected** содержит число записей, удаленных, обновленных или вставленных при выполнении запроса на изменение.</span><span class="sxs-lookup"><span data-stu-id="d2c11-152">For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query.</span></span> <span data-ttu-id="d2c11-153">Если метод **Execute** используется для выполнения запроса, в качестве значения свойства **RecordsAffected** объекта **QueryDef** устанавливается число затронутых записей.</span><span class="sxs-lookup"><span data-stu-id="d2c11-153">When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="d2c11-154">Когда в рабочей области Microsoft Access указана синтаксически правильная инструкция SQL и имеются соответствующие разрешения, метод **Execute** не приводит к сбою, даже если не удается изменить или удалить ни одну строку.</span><span class="sxs-lookup"><span data-stu-id="d2c11-154">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted.</span></span> <span data-ttu-id="d2c11-155">Поэтому всегда используйте параметр **dbFailOnError** при применении метода **Execute** для обновления или удаления запроса.</span><span class="sxs-lookup"><span data-stu-id="d2c11-155">Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query.</span></span> <span data-ttu-id="d2c11-156">Этот параметр создает ошибку во время выполнения и откатывает все успешно выполненные изменения, если какие-либо затронутые записи заблокированы и не могут быть обновлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="d2c11-156">This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="d2c11-157">В более ранних версиях ядра СУБД Microsoft Jet инструкции SQL автоматически внедрялись в неявные транзакции.</span><span class="sxs-lookup"><span data-stu-id="d2c11-157">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions.</span></span> <span data-ttu-id="d2c11-158">Если часть выполненной инструкции с параметром **dbFailOnError** приводила к сбою, выполнялся откат всей инструкции.</span><span class="sxs-lookup"><span data-stu-id="d2c11-158">If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back.</span></span> <span data-ttu-id="d2c11-159">Для повышения производительности эти неявные транзакции были удалены начиная с версии 3.5.</span><span class="sxs-lookup"><span data-stu-id="d2c11-159">To improve performance, these implicit transactions were removed starting with version 3.5.</span></span> <span data-ttu-id="d2c11-160">При обновлении более ранних версий кода DAO рассмотрите возможность использования явных транзакций с инструкциями **Execute**.</span><span class="sxs-lookup"><span data-stu-id="d2c11-160">If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="d2c11-161">Чтобы добиться оптимальной производительности в рабочей области Microsoft Access, особенно в многопользовательской среде, вложите метод **Execute** внутрь транзакции.</span><span class="sxs-lookup"><span data-stu-id="d2c11-161">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction.</span></span> <span data-ttu-id="d2c11-162">Используйте метод **BeginTrans** для текущего объекта **Workspace**, затем примените метод **Execute** и завершите транзакцию с помощью метода **CommitTrans** для объекта **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="d2c11-162">Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**.</span></span> <span data-ttu-id="d2c11-163">Это сохранит изменения на диске и освободит любые блокировки, установленные во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="d2c11-163">This saves changes on disk and frees any locks placed while the query is running.</span></span>

