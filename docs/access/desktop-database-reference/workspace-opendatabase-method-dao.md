---
title: Метод Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ca2ccb4183a59c2b579fd4375f26aa4fd539532f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700957"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="9bbb7-102">Метод Workspace.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="9bbb7-102">Workspace.OpenDatabase Method (DAO)</span></span>

<span data-ttu-id="9bbb7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bbb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bbb7-104">Открывает указанную базу данных в объекте \*\* [Workspace](workspace-object-dao.md) \*\* и возвращает ссылку на объект \*\* [Database](database-object-dao.md) \*\*, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bbb7-105">Syntax</span></span>

<span data-ttu-id="9bbb7-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="9bbb7-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="9bbb7-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-107">*expression* A variable that represents a **Range** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9bbb7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bbb7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bbb7-109">Имя</span><span class="sxs-lookup"><span data-stu-id="9bbb7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9bbb7-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="9bbb7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="9bbb7-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9bbb7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9bbb7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9bbb7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bbb7-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="9bbb7-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9bbb7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9bbb7-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="9bbb7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-116">Имя существующего файла ядра СУБД Microsoft Access или имя источника данных (DSN) для источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-116">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="9bbb7-117">См. свойство <strong> <a href="connection-name-property-dao.md">Name</a> </strong> для получения дополнительной информации о настройке данного значения.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bbb7-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="9bbb7-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-119">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="9bbb7-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9bbb7-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-121">Определяет различные опции для базы данных, согласно данным в Комментариях.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bbb7-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="9bbb7-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-123">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="9bbb7-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9bbb7-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-125">Установите значение <strong>True</strong>, если вы хотите открыть базу данных с правами доступа только для чтения, или <strong>False</strong> (установлено по умолчанию), если вы хотите открыть базу данных с правами доступа на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bbb7-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="9bbb7-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-127">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="9bbb7-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9bbb7-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-129">Определяет различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="9bbb7-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bbb7-130">Return value</span></span>

<span data-ttu-id="9bbb7-131">База данных</span><span class="sxs-lookup"><span data-stu-id="9bbb7-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="9bbb7-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bbb7-132">Remarks</span></span>

<span data-ttu-id="9bbb7-133">Вы можете использовать следующие значения для аргумента Options.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-133">You can use one of the following constants for the component argument:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bbb7-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="9bbb7-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="9bbb7-135">Описание</span><span class="sxs-lookup"><span data-stu-id="9bbb7-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bbb7-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="9bbb7-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-137">Открытие базы данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bbb7-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="9bbb7-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="9bbb7-139">(По умолчанию) Открытие базы данных в режиме совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="9bbb7-140">Когда вы открываете базу данных, она автоматически добавляется коллекцию **Databases**.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="9bbb7-141">Несколько советов в отношении применения dbname:</span><span class="sxs-lookup"><span data-stu-id="9bbb7-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="9bbb7-142">Если он ссылается на базу данных, которая уже открыта для доступа другому пользователю, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="9bbb7-143">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="9bbb7-144">Если он является строкой нулевой длины (""), а для *connect* установлено значение "ODBC;", откроется диалоговое окно со списком всех зарегистрированных имен источник данных ODBC, где пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="9bbb7-145">Чтобы закрыть базу данных, а значит удалить объект **Database** из коллекции **Databases**, используйте метод **[Close](connection-close-method-dao.md)** для объекта.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="9bbb7-146">При обращении к источнику данных ODBC, подключенного к ядру СУБД Microsoft Access вы можете повысить производительность вашего приложения, открыв объект **Database**, связанный с источником данных ODBC, не прибегая к связыванию отдельных объектов \*\* [TableDef](tabledef-object-dao.md) \*\* к определенным таблицам источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9bbb7-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="9bbb7-147">Пример</span><span class="sxs-lookup"><span data-stu-id="9bbb7-147">Example</span></span>

<span data-ttu-id="9bbb7-148">В этом примере используется метод **OpenDatabase** для открытия одной базы данных Microsoft Access и двух баз данных ODBC, подключенных к ядру СУБД Microsoft Access. </span><span class="sxs-lookup"><span data-stu-id="9bbb7-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

