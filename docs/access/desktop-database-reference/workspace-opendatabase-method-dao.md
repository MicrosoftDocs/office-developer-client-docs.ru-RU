---
title: Workspace.OpenDatabase Method (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05edf4979f7fe3a7084f2ab7a7b27f058447eac8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480575"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="1eaf4-102">Workspace.OpenDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="1eaf4-102">Workspace.OpenDatabase Method (DAO)</span></span>

<span data-ttu-id="1eaf4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1eaf4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1eaf4-104">Открывает указанной базы данных в объекте **[рабочей области](workspace-object-dao.md)** и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eaf4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eaf4-105">Syntax</span></span>

<span data-ttu-id="1eaf4-106">*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="1eaf4-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="1eaf4-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="1eaf4-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1eaf4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eaf4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1eaf4-109">Имя</span><span class="sxs-lookup"><span data-stu-id="1eaf4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1eaf4-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="1eaf4-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1eaf4-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1eaf4-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1eaf4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1eaf4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1eaf4-113">Имя</span><span class="sxs-lookup"><span data-stu-id="1eaf4-113">Name</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1eaf4-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="1eaf4-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1eaf4-116">Имя существующий файл базы данных ядра базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="1eaf4-116">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="1eaf4-117">Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="1eaf4-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1eaf4-118">Options</span><span class="sxs-lookup"><span data-stu-id="1eaf4-118">Options</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1eaf4-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1eaf4-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1eaf4-121">Задает различные параметры для базы данных, как указано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1eaf4-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1eaf4-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1eaf4-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1eaf4-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1eaf4-125"><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1eaf4-126">Подключение</span><span class="sxs-lookup"><span data-stu-id="1eaf4-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1eaf4-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="1eaf4-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1eaf4-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1eaf4-129">Указывает различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="1eaf4-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1eaf4-130">Return Value</span></span>

<span data-ttu-id="1eaf4-131">База данных</span><span class="sxs-lookup"><span data-stu-id="1eaf4-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="1eaf4-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="1eaf4-132">Remarks</span></span>

<span data-ttu-id="1eaf4-133">Можно использовать следующие значения для аргумента options.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1eaf4-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="1eaf4-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="1eaf4-135">Описание</span><span class="sxs-lookup"><span data-stu-id="1eaf4-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1eaf4-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="1eaf4-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="1eaf4-137">Открывает базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1eaf4-138"><strong>Значение false</strong></span><span class="sxs-lookup"><span data-stu-id="1eaf4-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="1eaf4-139">(По умолчанию) Открывает базу данных в режиме общего доступа.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1eaf4-140">При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="1eaf4-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="1eaf4-141">Некоторые соображения при использовании dbname.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="1eaf4-142">Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="1eaf4-143">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="1eaf4-144">Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="1eaf4-145">Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="1eaf4-146">При получении доступа к Microsoft access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта **базы данных** , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов **[TableDef](tabledef-object-dao.md)** в определенных в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="1eaf4-147">Пример</span><span class="sxs-lookup"><span data-stu-id="1eaf4-147">Example</span></span>

<span data-ttu-id="1eaf4-148">В этом примере используется метод **OpenDatabase** для открытия базы данных подключен модуль ODBC два Microsoft Access базы данных и одна база данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1eaf4-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

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

