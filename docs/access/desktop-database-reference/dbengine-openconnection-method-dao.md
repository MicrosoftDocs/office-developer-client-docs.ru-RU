---
title: DBEngine.OpenConnection Method (DAO)
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
ms.openlocfilehash: 959291193b8606ce223e6ad1a20c17895b136a13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876794"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="20758-102">DBEngine.OpenConnection Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="20758-102">DBEngine.OpenConnection Method (DAO)</span></span>


<span data-ttu-id="20758-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20758-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="20758-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20758-104">Syntax</span></span>

<span data-ttu-id="20758-105">*выражение* . OpenConnection (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="20758-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="20758-106">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="20758-106">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="20758-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20758-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20758-108">Имя</span><span class="sxs-lookup"><span data-stu-id="20758-108">Name</span></span></p></th>
<th><p><span data-ttu-id="20758-109">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="20758-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="20758-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="20758-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="20758-111">Описание</span><span class="sxs-lookup"><span data-stu-id="20758-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20758-112">Имя</span><span class="sxs-lookup"><span data-stu-id="20758-112">Name</span></span></p></td>
<td><p><span data-ttu-id="20758-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="20758-113">Required</span></span></p></td>
<td><p><span data-ttu-id="20758-114"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="20758-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-115">Строковое выражение.</span><span class="sxs-lookup"><span data-stu-id="20758-115">A string expression.</span></span> <span data-ttu-id="20758-116">В разделе обсуждения в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="20758-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20758-117">Options</span><span class="sxs-lookup"><span data-stu-id="20758-117">Options</span></span></p></td>
<td><p><span data-ttu-id="20758-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20758-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="20758-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20758-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-120">Задает различные параметры подключения, как указано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="20758-120">sets various options for the connection, as specified in Remarks.</span></span> <span data-ttu-id="20758-121">На основе этого значения, драйвера ODBC запрашивает сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="20758-121">Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20758-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="20758-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="20758-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20758-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="20758-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20758-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-125"><strong>Значение true,</strong> Если подключение будет открыт для доступа только для чтения и <strong>значение False</strong> , если подключение должен быть открыт для чтения и записи (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="20758-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20758-126">Подключение</span><span class="sxs-lookup"><span data-stu-id="20758-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="20758-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20758-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="20758-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20758-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-129">Строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="20758-129">An ODBC connection string.</span></span> <span data-ttu-id="20758-130">В разделе свойства <strong><a href="connection-connect-property-dao.md">подключения</a></strong> для определенных элементов и синтаксис этой строки.</span><span class="sxs-lookup"><span data-stu-id="20758-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="20758-131">Начале стоит символ &quot;ODBC. &quot; является обязательным.</span><span class="sxs-lookup"><span data-stu-id="20758-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="20758-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20758-132">Return value</span></span>

<span data-ttu-id="20758-133">Подключение</span><span class="sxs-lookup"><span data-stu-id="20758-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="20758-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="20758-134">Remarks</span></span>

<span data-ttu-id="20758-135">Используйте метод **OpenConnection** для подключения к источнику данных ODBC из рабочей области технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="20758-135">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace.</span></span> <span data-ttu-id="20758-136">Метод **OpenConnection** похоже, но не эквивалентно **OpenDatabase**.</span><span class="sxs-lookup"><span data-stu-id="20758-136">The **OpenConnection** method is similar but not equivalent to **OpenDatabase**.</span></span> <span data-ttu-id="20758-137">Основное различие — это **OpenConnection** доступны только в рабочей области технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="20758-137">The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="20758-138">Если указать зарегистрированных имя источника данных ODBC (DSN) в аргументе подключиться, а затем может быть любое допустимое строковое аргумента имени, а также предоставляют свойства **Name** для объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="20758-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="20758-139">Если допустимый уведомления о Доставке не включен в аргументе подключение, имя должны ссылаться на допустимый ODBC DSN, которая также будет свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="20758-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="20758-140">Если имя ни подключения содержит допустимое уведомления о Доставке драйвера ODBC может быть установлено (с помощью аргумента options) запрашивать у пользователя необходимые сведения для соединения.</span><span class="sxs-lookup"><span data-stu-id="20758-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="20758-141">Уведомления о Доставке обеспечиваться на строке, затем предоставляет свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="20758-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="20758-142">Параметры аргумент определяет, если и когда запрос пользователю для установления подключения, а ли асинхронно открытия подключения.</span><span class="sxs-lookup"><span data-stu-id="20758-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="20758-143">Можно использовать один из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="20758-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20758-144">Константа</span><span class="sxs-lookup"><span data-stu-id="20758-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="20758-145">Описание</span><span class="sxs-lookup"><span data-stu-id="20758-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20758-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="20758-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-147">Драйвера ODBC использует строку подключения, представленные в <em>dbname</em> и <em>подключения</em>.</span><span class="sxs-lookup"><span data-stu-id="20758-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="20758-148">Если не предоставляют достаточно сведений, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="20758-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20758-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="20758-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-150">Драйвера ODBC отображает диалоговое окно <strong>Источники данных ODBC</strong> , в которой отображаются все соответствующие сведения указано в <em>dbname</em> или <em>подключиться</em>.</span><span class="sxs-lookup"><span data-stu-id="20758-150">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>.</span></span> <span data-ttu-id="20758-151">Строка подключения состоит из источника данных, что пользователь выбирает с помощью диалоговых окон, или, если пользователь не указывает имя источника данных, используется значение по умолчанию уведомления о Доставке.</span><span class="sxs-lookup"><span data-stu-id="20758-151">The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20758-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="20758-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-153">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20758-153">Default.</span></span> <span data-ttu-id="20758-154">Если аргумент <em>подключения</em> содержит все необходимые сведения для выполнения подключения, драйвера ODBC использует строку в <em>подключение</em>.</span><span class="sxs-lookup"><span data-stu-id="20758-154">If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>.</span></span> <span data-ttu-id="20758-155">В противном случае оно ведет себя как при указании <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="20758-155">Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20758-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="20758-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-157">Этот параметр действует как <strong>dbDriverComplete</strong> , за исключением драйвер ODBC отключает запрашивала какие-либо сведения для выполнения подключения не требуется.</span><span class="sxs-lookup"><span data-stu-id="20758-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20758-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="20758-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="20758-159">Асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="20758-159">Execute the method asynchronously.</span></span> <span data-ttu-id="20758-160">В этом константы могут быть использованы с любыми другими константы <em>Параметры</em> .</span><span class="sxs-lookup"><span data-stu-id="20758-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20758-161">**OpenConnection** возвращает объект **подключения** , который содержит сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="20758-161">**OpenConnection** returns a **Connection** object which contains information about the connection.</span></span> <span data-ttu-id="20758-162">Объект **подключения** аналогичен объекта **[базы данных](database-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="20758-162">The **Connection** object is similar to a **[Database](database-object-dao.md)** object.</span></span> <span data-ttu-id="20758-163">Участника отличие заключается в том, что объект **базы данных** обычно представляет базы данных, несмотря на то, что его можно использовать для представления подключения к источнику данных ODBC из рабочей области для Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="20758-163">The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

