---
title: Метод DBEngine.OpenConnection (DAO)
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
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="f31a7-102">Метод DBEngine.OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="f31a7-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="f31a7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f31a7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f31a7-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f31a7-104">Syntax</span></span>

<span data-ttu-id="f31a7-105">*выражения* . OpenConnection (***Имя***, ***Параметры***, ***ReadOnly***, ***Подключение***)</span><span class="sxs-lookup"><span data-stu-id="f31a7-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="f31a7-106">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="f31a7-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f31a7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f31a7-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f31a7-108">Имя</span><span class="sxs-lookup"><span data-stu-id="f31a7-108">Name</span></span></p></th>
<th><p><span data-ttu-id="f31a7-109">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="f31a7-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f31a7-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f31a7-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="f31a7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f31a7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f31a7-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="f31a7-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f31a7-113">Required</span></span></p></td>
<td><p><span data-ttu-id="f31a7-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-115">Строковое выражение.</span><span class="sxs-lookup"><span data-stu-id="f31a7-115">A string expression.</span></span> <span data-ttu-id="f31a7-116">См. в статье Примечание.</span><span class="sxs-lookup"><span data-stu-id="f31a7-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31a7-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="f31a7-118">Необязательно</span><span class="sxs-lookup"><span data-stu-id="f31a7-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="f31a7-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-120">задает различные параметры подключения, как указано в Примечание.</span><span class="sxs-lookup"><span data-stu-id="f31a7-120">sets various options for the connection, as specified in Remarks.</span></span> <span data-ttu-id="f31a7-121">На основе этого значения диспетчер драйверов ODBC подсказывит пользователю сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="f31a7-121">Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31a7-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="f31a7-123">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="f31a7-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="f31a7-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-125"><strong>True,</strong> если подключение должно быть открыто для доступа только для чтения и <strong>false,</strong> если подключение должно быть открыто для чтения и записи доступа (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f31a7-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31a7-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="f31a7-127">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="f31a7-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="f31a7-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-129">Строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="f31a7-129">An ODBC connection string.</span></span> <span data-ttu-id="f31a7-130">См. <strong><a href="connection-connect-property-dao.md">Подключение</a></strong> свойства для определенных элементов и синтаксиса этой строки.</span><span class="sxs-lookup"><span data-stu-id="f31a7-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="f31a7-131">Необходимо предварительное &quot; ODBC. &quot;</span><span class="sxs-lookup"><span data-stu-id="f31a7-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="f31a7-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f31a7-132">Return value</span></span>

<span data-ttu-id="f31a7-133">Connection</span><span class="sxs-lookup"><span data-stu-id="f31a7-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="f31a7-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="f31a7-134">Remarks</span></span>

<span data-ttu-id="f31a7-135">Используйте метод **OpenConnection** для подключения к источнику данных ODBC из рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="f31a7-135">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace.</span></span> <span data-ttu-id="f31a7-136">Метод **OpenConnection** похож, но не эквивалентен **OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="f31a7-136">The **OpenConnection** method is similar but not equivalent to **OpenDatabase**.</span></span> <span data-ttu-id="f31a7-137">Главное отличие заключается в том, что **OpenConnection** доступен только в рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="f31a7-137">The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="f31a7-138">Если в аргументе подключения указывается зарегистрированное имя источника данных ODBC (DSN), аргумент имени может быть любой допустимой строкой, а также будет предоставлять свойство **Name** для объекта **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="f31a7-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="f31a7-139">Если допустимая DSN не включена в аргумент подключения, то имя должно ссылаться на допустимый DSN ODBC, который также будет **свойством Name.**</span><span class="sxs-lookup"><span data-stu-id="f31a7-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="f31a7-140">Если ни имя, ни подключение не содержат допустимой DSN, диспетчер драйвера ODBC может быть задат (с помощью аргумента параметра) для запроса пользователем необходимых сведений о подключении.</span><span class="sxs-lookup"><span data-stu-id="f31a7-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="f31a7-141">DSN, поставляемая через запрос, затем предоставляет **свойство Name.**</span><span class="sxs-lookup"><span data-stu-id="f31a7-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="f31a7-142">Аргумент параметров определяет, следует ли и когда побудить пользователя установить подключение и открыть ли подключение асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f31a7-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="f31a7-143">Можно использовать одну из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="f31a7-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f31a7-144">Константа</span><span class="sxs-lookup"><span data-stu-id="f31a7-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="f31a7-145">Описание</span><span class="sxs-lookup"><span data-stu-id="f31a7-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f31a7-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-147">Диспетчер драйверов ODBC использует строку подключения, предоставленную <em>в dbname</em> и <em>подключаемую.</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="f31a7-148">Если вы не предоставляете достаточных сведений, возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="f31a7-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31a7-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-150">Диспетчер драйверов ODBC отображает диалоговое окно <strong>ODBC Data Sources,</strong> в котором отображаются все релевантные сведения, предоставленные в <em>dbname</em> или <em>соедините.</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-150">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>.</span></span> <span data-ttu-id="f31a7-151">Строка подключения состоит из DSN, который пользователь выбирает через диалоговое окно, или, если пользователь не указывает DSN, используется DSN по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f31a7-151">The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31a7-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-153">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f31a7-153">Default.</span></span> <span data-ttu-id="f31a7-154">Если аргумент <em>подключения</em> включает все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в <em>соединении.</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-154">If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>.</span></span> <span data-ttu-id="f31a7-155">В противном случае он ведет себя так же, как и при указании <strong>dbDriverPrompt.</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-155">Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f31a7-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-157">Этот параметр ведет себя как <strong>dbDriverComplete,</strong> за исключением того, что драйвер ODBC отключает запросы для получения любых сведений, не необходимых для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="f31a7-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f31a7-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="f31a7-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="f31a7-159">Выполните метод асинхронно.</span><span class="sxs-lookup"><span data-stu-id="f31a7-159">Execute the method asynchronously.</span></span> <span data-ttu-id="f31a7-160">Эта константа может использоваться с любыми другими константами <em>параметров.</em></span><span class="sxs-lookup"><span data-stu-id="f31a7-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f31a7-161">**OpenConnection** возвращает объект **Connection,** содержащий сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="f31a7-161">**OpenConnection** returns a **Connection** object which contains information about the connection.</span></span> <span data-ttu-id="f31a7-162">Объект **Connection** похож на объект **[Database.](database-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="f31a7-162">The **Connection** object is similar to a **[Database](database-object-dao.md)** object.</span></span> <span data-ttu-id="f31a7-163">Основное отличие состоит в том, что объект **Database** обычно представляет базу данных, хотя ее можно использовать для представления подключения к источнику данных ODBC из рабочего пространства Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f31a7-163">The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

