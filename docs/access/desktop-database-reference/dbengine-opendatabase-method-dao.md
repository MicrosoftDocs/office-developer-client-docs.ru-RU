---
title: DBEngine.OpenDatabase Method (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 54078705c67e892b80a08ce2bd31db191c7fc70c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606160"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="0cb4c-102">DBEngine.OpenDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="0cb4c-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="0cb4c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cb4c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0cb4c-104">Открывает указанной базы данных и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cb4c-105">Syntax</span></span>

<span data-ttu-id="0cb4c-106">*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="0cb4c-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="0cb4c-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0cb4c-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0cb4c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cb4c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0cb4c-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0cb4c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0cb4c-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="0cb4c-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0cb4c-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0cb4c-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0cb4c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb4c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cb4c-113">Имя</span><span class="sxs-lookup"><span data-stu-id="0cb4c-113">Name</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0cb4c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="0cb4c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb4c-116">имя существующего файла базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="0cb4c-116">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="0cb4c-117">Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="0cb4c-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb4c-118">Options</span><span class="sxs-lookup"><span data-stu-id="0cb4c-118">Options</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0cb4c-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0cb4c-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb4c-121">Задает различные параметры для базы данных, как указано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb4c-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0cb4c-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0cb4c-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0cb4c-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb4c-125"><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb4c-126">Подключение</span><span class="sxs-lookup"><span data-stu-id="0cb4c-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0cb4c-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="0cb4c-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0cb4c-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb4c-129">Указывает различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cb4c-130"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0cb4c-130"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="0cb4c-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cb4c-131">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="0cb4c-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cb4c-132">Return value</span></span>
>>>>>>> <span data-ttu-id="0cb4c-133">master</span><span class="sxs-lookup"><span data-stu-id="0cb4c-133">master</span></span>

<span data-ttu-id="0cb4c-134">База данных</span><span class="sxs-lookup"><span data-stu-id="0cb4c-134">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb4c-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="0cb4c-135">Remarks</span></span>

<span data-ttu-id="0cb4c-136">Можно использовать следующие значения для аргумента options.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-136">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0cb4c-137">Параметр</span><span class="sxs-lookup"><span data-stu-id="0cb4c-137">Setting</span></span></p></th>
<th><p><span data-ttu-id="0cb4c-138">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb4c-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cb4c-139"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="0cb4c-139"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb4c-140">Открывает базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-140">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb4c-141"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="0cb4c-141"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="0cb4c-142">(По умолчанию) Открывает базу данных в режиме общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-142">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cb4c-143">При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="0cb4c-143">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="0cb4c-144">Некоторые соображения при использовании dbname.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-144">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="0cb4c-145">Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-145">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="0cb4c-146">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-146">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="0cb4c-147">Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-147">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="0cb4c-148">Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-148">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0cb4c-149">При получении доступа к Microsoft Access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта <STRONG>базы данных</STRONG> , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> в определенных в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0cb4c-149">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a <STRONG>Database</STRONG> object connected to the ODBC data source, rather than by linking individual <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> objects to specific tables in the ODBC data source.</span></span></P>


