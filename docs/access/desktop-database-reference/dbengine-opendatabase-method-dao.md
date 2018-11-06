---
title: Метод DBEngine.OpenDatabase (DAO)
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
ms.openlocfilehash: a00c61ce4cbb9cb9d6088d521f0c2bdb3cf7f573
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998077"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="8e864-102">Метод DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e864-102">DBEngine.OpenDatabase method (DAO)</span></span>

<span data-ttu-id="8e864-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e864-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e864-104">Открывает указанной базы данных и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="8e864-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e864-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e864-105">Syntax</span></span>

<span data-ttu-id="8e864-106">*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="8e864-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="8e864-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="8e864-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e864-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e864-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e864-109">Имя</span><span class="sxs-lookup"><span data-stu-id="8e864-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8e864-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="8e864-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8e864-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8e864-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8e864-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8e864-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e864-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8e864-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8e864-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8e864-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8e864-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="8e864-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8e864-116">имя существующего файла базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="8e864-116">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="8e864-117">Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="8e864-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e864-118"><em>Варианты</em></span><span class="sxs-lookup"><span data-stu-id="8e864-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="8e864-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8e864-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="8e864-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8e864-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8e864-121">Задает различные параметры для базы данных, как указано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="8e864-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e864-122"><em>Только для чтения</em></span><span class="sxs-lookup"><span data-stu-id="8e864-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="8e864-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8e864-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="8e864-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8e864-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8e864-125"><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="8e864-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e864-126"><em>Подключение</em></span><span class="sxs-lookup"><span data-stu-id="8e864-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="8e864-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8e864-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="8e864-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8e864-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8e864-129">Указывает различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="8e864-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="8e864-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e864-130">Return value</span></span>

<span data-ttu-id="8e864-131">База данных</span><span class="sxs-lookup"><span data-stu-id="8e864-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="8e864-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e864-132">Remarks</span></span>

<span data-ttu-id="8e864-133">Можно использовать следующие значения для аргумента options.</span><span class="sxs-lookup"><span data-stu-id="8e864-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e864-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="8e864-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="8e864-135">Описание</span><span class="sxs-lookup"><span data-stu-id="8e864-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e864-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="8e864-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="8e864-137">Открывает базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="8e864-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e864-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="8e864-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="8e864-139">(По умолчанию) Открывает базу данных в режиме общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8e864-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e864-140">При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="8e864-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="8e864-141">Некоторые соображения при использовании dbname.</span><span class="sxs-lookup"><span data-stu-id="8e864-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="8e864-142">Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8e864-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="8e864-143">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8e864-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="8e864-144">Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="8e864-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="8e864-145">Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.</span><span class="sxs-lookup"><span data-stu-id="8e864-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="8e864-146">При получении доступа к Microsoft Access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта **базы данных** , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов [TableDef](tabledef-object-dao.md) в определенных в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="8e864-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


