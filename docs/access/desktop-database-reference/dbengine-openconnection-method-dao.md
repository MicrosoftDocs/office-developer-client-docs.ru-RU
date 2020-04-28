---
title: Метод DBEngine. OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294262"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="55edc-102">Метод DBEngine. OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="55edc-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="55edc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55edc-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="55edc-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55edc-104">Syntax</span></span>

<span data-ttu-id="55edc-105">*Expression* . OpenConnection (***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="55edc-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="55edc-106">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="55edc-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="55edc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="55edc-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55edc-108">Имя</span><span class="sxs-lookup"><span data-stu-id="55edc-108">Name</span></span></p></th>
<th><p><span data-ttu-id="55edc-109">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="55edc-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="55edc-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="55edc-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="55edc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="55edc-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55edc-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="55edc-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="55edc-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55edc-113">Required</span></span></p></td>
<td><p><span data-ttu-id="55edc-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-115">Строковое выражение.</span><span class="sxs-lookup"><span data-stu-id="55edc-115">A string expression.</span></span> <span data-ttu-id="55edc-116">Просмотрите обсуждение в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="55edc-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55edc-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="55edc-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="55edc-118">Необязательно</span><span class="sxs-lookup"><span data-stu-id="55edc-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="55edc-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-120">Задает различные параметры подключения, как указано в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="55edc-120">sets various options for the connection, as specified in Remarks.</span></span> <span data-ttu-id="55edc-121">На основе этого значения диспетчер драйверов ODBC запрашивает у пользователя сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="55edc-121">Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55edc-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="55edc-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="55edc-123">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="55edc-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="55edc-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-125"><strong>Имеет значение true</strong> , если подключение должно быть открыто только для чтения, и <strong>false</strong> , если подключение должно быть открыто для чтения и записи (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="55edc-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55edc-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="55edc-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="55edc-127">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="55edc-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="55edc-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-129">Строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="55edc-129">An ODBC connection string.</span></span> <span data-ttu-id="55edc-130">Просмотрите свойство <strong><a href="connection-connect-property-dao.md">Connect</a></strong> для определенных элементов и синтаксиса этой строки.</span><span class="sxs-lookup"><span data-stu-id="55edc-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="55edc-131">Префикс &quot;ODBC; &quot; является обязательным.</span><span class="sxs-lookup"><span data-stu-id="55edc-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="55edc-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55edc-132">Return value</span></span>

<span data-ttu-id="55edc-133">Connection</span><span class="sxs-lookup"><span data-stu-id="55edc-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="55edc-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="55edc-134">Remarks</span></span>

<span data-ttu-id="55edc-135">Используйте метод **OpenConnection** , чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="55edc-135">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace.</span></span> <span data-ttu-id="55edc-136">Метод **OpenConnection** аналогичен, но не эквивалентен **openDatabase**.</span><span class="sxs-lookup"><span data-stu-id="55edc-136">The **OpenConnection** method is similar but not equivalent to **OpenDatabase**.</span></span> <span data-ttu-id="55edc-137">Основное отличие состоит в том, что **OpenConnection** доступно только в рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="55edc-137">The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="55edc-138">Если указать в аргументе Connect имя зарегистрированного источника данных ODBC (DSN), то аргумент name может быть любой допустимой строкой, а также будет предоставлять свойство **Name** для объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="55edc-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="55edc-139">Если допустимое имя DSN не включено в аргумент Connect, то имя должно ссылаться на допустимый DSN ODBC, которое также будет являться свойством **Name** .</span><span class="sxs-lookup"><span data-stu-id="55edc-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="55edc-140">Если ни одно из этих имен и не содержит допустимое имя DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента Options), чтобы запросить у пользователя необходимые сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="55edc-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="55edc-141">Имя источника данных, предоставляемое при высказке, предоставляет свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="55edc-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="55edc-142">Аргумент options определяет, когда и когда следует предлагать пользователю установить подключение, а также следует ли асинхронно открывать подключение.</span><span class="sxs-lookup"><span data-stu-id="55edc-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="55edc-143">Можно использовать одну из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="55edc-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55edc-144">Константа</span><span class="sxs-lookup"><span data-stu-id="55edc-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="55edc-145">Описание</span><span class="sxs-lookup"><span data-stu-id="55edc-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55edc-146"><strong>дбдривернопромпт</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-147">Диспетчер драйверов ODBC использует строку подключения, указанную в <em>dbname</em> и <em>Connect</em>.</span><span class="sxs-lookup"><span data-stu-id="55edc-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="55edc-148">Если вы не выдаете достаточно сведений, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="55edc-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55edc-149"><strong>дбдриверпромпт</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-150">Диспетчер драйверов ODBC отображает диалоговое окно <strong>Источники данных ODBC</strong> , в котором отображаются все релевантные сведения, предоставленные в <em>dbname</em> или <em>Connect</em>.</span><span class="sxs-lookup"><span data-stu-id="55edc-150">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>.</span></span> <span data-ttu-id="55edc-151">Строка подключения состоит из имени источника данных, которое пользователь выбрал через диалоговые окна, или, если пользователь не указал значение DSN, используется DSN по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="55edc-151">The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55edc-152"><strong>дбдриверкомплете</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-153">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="55edc-153">Default.</span></span> <span data-ttu-id="55edc-154">Если аргумент <em>Connect</em> включает все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в разделе <em>Connect</em>.</span><span class="sxs-lookup"><span data-stu-id="55edc-154">If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>.</span></span> <span data-ttu-id="55edc-155">В противном случае он ведет себя так же, как и при указании <strong>дбдриверпромпт</strong>.</span><span class="sxs-lookup"><span data-stu-id="55edc-155">Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55edc-156"><strong>дбдриверкомплетерекуиред</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-157">Этот параметр имеет вид <strong>дбдриверкомплете</strong> , за исключением того, что в ДРАЙВЕРе ODBC отключается запрос для получения сведений, не необходимых для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="55edc-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55edc-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="55edc-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="55edc-159">Асинхронно выполняет метод.</span><span class="sxs-lookup"><span data-stu-id="55edc-159">Execute the method asynchronously.</span></span> <span data-ttu-id="55edc-160">Эту константу можно использовать с любыми другими константами <em>Options</em> .</span><span class="sxs-lookup"><span data-stu-id="55edc-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55edc-161">**OpenConnection** возвращает объект **Connection** , который содержит сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="55edc-161">**OpenConnection** returns a **Connection** object which contains information about the connection.</span></span> <span data-ttu-id="55edc-162">Объект **Connection** аналогичен объекту **[базы данных](database-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="55edc-162">The **Connection** object is similar to a **[Database](database-object-dao.md)** object.</span></span> <span data-ttu-id="55edc-163">Основное различие состоит в том, что объект **базы данных** обычно представляет базу данных, хотя он может использоваться для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="55edc-163">The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

