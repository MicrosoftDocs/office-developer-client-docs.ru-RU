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
ms.openlocfilehash: 45075a612b5d8dc6fabd4a91cc1efdacf37874a0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878943"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="a1d5e-102">DBEngine.OpenDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1d5e-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="a1d5e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1d5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1d5e-104">Открывает указанной базы данных и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d5e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1d5e-105">Syntax</span></span>

<span data-ttu-id="a1d5e-106">*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="a1d5e-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="a1d5e-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="a1d5e-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a1d5e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1d5e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1d5e-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a1d5e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a1d5e-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a1d5e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a1d5e-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a1d5e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a1d5e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a1d5e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1d5e-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a1d5e-113">Name</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a1d5e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="a1d5e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a1d5e-116">имя существующего файла базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="a1d5e-116">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="a1d5e-117">Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="a1d5e-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1d5e-118">Options</span><span class="sxs-lookup"><span data-stu-id="a1d5e-118">Options</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a1d5e-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a1d5e-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a1d5e-121">Задает различные параметры для базы данных, как указано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1d5e-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a1d5e-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a1d5e-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a1d5e-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a1d5e-125"><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1d5e-126">Подключение</span><span class="sxs-lookup"><span data-stu-id="a1d5e-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a1d5e-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="a1d5e-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a1d5e-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a1d5e-129">Указывает различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a1d5e-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1d5e-130">Return value</span></span>

<span data-ttu-id="a1d5e-131">База данных</span><span class="sxs-lookup"><span data-stu-id="a1d5e-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d5e-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1d5e-132">Remarks</span></span>

<span data-ttu-id="a1d5e-133">Можно использовать следующие значения для аргумента options.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1d5e-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="a1d5e-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="a1d5e-135">Описание</span><span class="sxs-lookup"><span data-stu-id="a1d5e-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1d5e-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="a1d5e-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="a1d5e-137">Открывает базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1d5e-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="a1d5e-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="a1d5e-139">(По умолчанию) Открывает базу данных в режиме общего доступа.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1d5e-140">При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="a1d5e-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="a1d5e-141">Некоторые соображения при использовании dbname.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-141">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="a1d5e-142">Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="a1d5e-143">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="a1d5e-144">Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="a1d5e-145">Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <span data-ttu-id="a1d5e-146">При получении доступа к Microsoft Access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта **базы данных** , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов [TableDef](tabledef-object-dao.md) в определенных в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a1d5e-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


