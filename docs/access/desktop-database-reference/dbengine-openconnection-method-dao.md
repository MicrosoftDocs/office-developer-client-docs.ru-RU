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
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="1bbc2-102">Метод DBEngine.OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="1bbc2-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="1bbc2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bbc2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1bbc2-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bbc2-104">Syntax</span></span>

<span data-ttu-id="1bbc2-105">*выражение .* OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="1bbc2-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="1bbc2-106">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1bbc2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bbc2-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1bbc2-108">Имя</span><span class="sxs-lookup"><span data-stu-id="1bbc2-108">Name</span></span></p></th>
<th><p><span data-ttu-id="1bbc2-109">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="1bbc2-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1bbc2-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1bbc2-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="1bbc2-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1bbc2-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bbc2-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1bbc2-113">Required</span></span></p></td>
<td><p><span data-ttu-id="1bbc2-114"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-115">Строковое выражение.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-115">A string expression.</span></span> <span data-ttu-id="1bbc2-116">См. обсуждение в статье "Замечания".</span><span class="sxs-lookup"><span data-stu-id="1bbc2-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bbc2-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-118">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1bbc2-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="1bbc2-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-120">задает различные параметры подключения, как указано в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-120">sets various options for the connection, as specified in Remarks.</span></span> <span data-ttu-id="1bbc2-121">На основе этого значения диспетчер драйверов ODBC запросит у пользователя такие сведения о под подключением, как имя источника данных (DSN), имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-121">Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bbc2-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-123">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="1bbc2-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-125">Имеет значение <strong>True,</strong> если подключение должно быть открыто только для чтения, и <strong>False,</strong> если подключение должно быть открыто для чтения и записи (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1bbc2-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bbc2-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-127">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="1bbc2-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-129">Строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-129">An ODBC connection string.</span></span> <span data-ttu-id="1bbc2-130">См. <strong><a href="connection-connect-property-dao.md">свойство Connect</a></strong> для определенных элементов и синтаксиса этой строки.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="1bbc2-131">Предварительное &quot; ODBC; &quot; является обязательной.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="1bbc2-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bbc2-132">Return value</span></span>

<span data-ttu-id="1bbc2-133">Connection</span><span class="sxs-lookup"><span data-stu-id="1bbc2-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="1bbc2-134">Заметки</span><span class="sxs-lookup"><span data-stu-id="1bbc2-134">Remarks</span></span>

<span data-ttu-id="1bbc2-135">Используйте метод **OpenConnection,** чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-135">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace.</span></span> <span data-ttu-id="1bbc2-136">Метод **OpenConnection** похож, но не эквивалентен **Методу OpenDatabase.**</span><span class="sxs-lookup"><span data-stu-id="1bbc2-136">The **OpenConnection** method is similar but not equivalent to **OpenDatabase**.</span></span> <span data-ttu-id="1bbc2-137">Основное отличие заключается в **том, что OpenConnection** доступен только в рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-137">The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="1bbc2-138">Если в аргументе подключения указывается зарегистрированное имя источника данных ODBC (DSN), аргументом имени может быть любая допустимая строка, а также предоставляется свойство **Name** для объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="1bbc2-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="1bbc2-139">Если допустимое DSN не включено в аргумент подключения, имя должно ссылаться на допустимое DSN ODBC, которое также будет **свойством Name.**</span><span class="sxs-lookup"><span data-stu-id="1bbc2-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="1bbc2-140">Если ни имя, ни подключение не содержат допустимое DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента параметров), чтобы задействовать у пользователя необходимые сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="1bbc2-141">Затем DSN, предоставленное по запросу, предоставляет **свойство Name.**</span><span class="sxs-lookup"><span data-stu-id="1bbc2-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="1bbc2-142">Аргумент options определяет, следует ли и когда пользователю предложено установить подключение, а также следует ли открывать подключение асинхронно.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="1bbc2-143">Можно использовать одну из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1bbc2-144">Константа</span><span class="sxs-lookup"><span data-stu-id="1bbc2-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="1bbc2-145">Описание</span><span class="sxs-lookup"><span data-stu-id="1bbc2-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bbc2-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-147">Диспетчер драйверов ODBC использует строку подключения, предоставленную <em>в имени dbname</em> и <em>connect.</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="1bbc2-148">Если у вас недостаточно сведений, возникает ошибка во время запуска.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bbc2-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-150">В диспетчере драйверов ODBC отображается диалоговое окно "Источники данных <strong>ODBC",</strong> в котором отображаются все необходимые сведения, предоставленные в <em>имени dbname</em> или <em>connect.</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-150">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>.</span></span> <span data-ttu-id="1bbc2-151">Строка подключения состоит из DSN, выбранного пользователем через диалоговое окно, или, если пользователь не указывает DSN, используется DSN по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-151">The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bbc2-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-153">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-153">Default.</span></span> <span data-ttu-id="1bbc2-154">Если аргумент <em>подключения</em> содержит все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в <em>подключении.</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-154">If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>.</span></span> <span data-ttu-id="1bbc2-155">В противном случае он будет вести себя так же, как при <strong>указании dbDriverPrompt.</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-155">Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bbc2-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-157">Этот параметр работает так же, как <strong>и dbDriverComplete,</strong> за исключением того, что драйвер ODBC отключает запросы на все сведения, не необходимые для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bbc2-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="1bbc2-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="1bbc2-159">Выполните метод асинхронно.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-159">Execute the method asynchronously.</span></span> <span data-ttu-id="1bbc2-160">Эта константа может использоваться с любыми другими <em>константами параметров.</em></span><span class="sxs-lookup"><span data-stu-id="1bbc2-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1bbc2-161">**OpenConnection** возвращает объект **Connection,** содержащий сведения о подсети.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-161">**OpenConnection** returns a **Connection** object which contains information about the connection.</span></span> <span data-ttu-id="1bbc2-162">Объект **Connection** похож на объект **[Database.](database-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="1bbc2-162">The **Connection** object is similar to a **[Database](database-object-dao.md)** object.</span></span> <span data-ttu-id="1bbc2-163">Основное отличие состоит в том, что объект **Database** обычно представляет базу данных, хотя его можно использовать для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1bbc2-163">The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

