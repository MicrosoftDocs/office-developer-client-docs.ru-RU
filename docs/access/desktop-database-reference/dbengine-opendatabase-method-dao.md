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
ms.openlocfilehash: 311481a83c25df29a26610a979a67ceb38124470
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860422"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="c7df2-102">DBEngine.OpenDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="c7df2-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="c7df2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7df2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c7df2-104">Открывает указанной базы данных и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="c7df2-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7df2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7df2-105">Syntax</span></span>

<span data-ttu-id="c7df2-106">*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="c7df2-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="c7df2-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="c7df2-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c7df2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7df2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7df2-109">Имя</span><span class="sxs-lookup"><span data-stu-id="c7df2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c7df2-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="c7df2-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c7df2-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c7df2-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c7df2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c7df2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7df2-113">Имя</span><span class="sxs-lookup"><span data-stu-id="c7df2-113">Name</span></span></p></td>
<td><p><span data-ttu-id="c7df2-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c7df2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c7df2-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="c7df2-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c7df2-116">имя существующего файла базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="c7df2-116">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="c7df2-117">Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="c7df2-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7df2-118">Options</span><span class="sxs-lookup"><span data-stu-id="c7df2-118">Options</span></span></p></td>
<td><p><span data-ttu-id="c7df2-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c7df2-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="c7df2-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c7df2-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c7df2-121">Задает различные параметры для базы данных, как указано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="c7df2-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7df2-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c7df2-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="c7df2-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c7df2-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="c7df2-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c7df2-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c7df2-125"><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c7df2-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7df2-126">Подключение</span><span class="sxs-lookup"><span data-stu-id="c7df2-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="c7df2-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c7df2-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="c7df2-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c7df2-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c7df2-129">Указывает различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="c7df2-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7df2-130"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="c7df2-130"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="c7df2-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7df2-131">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="c7df2-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7df2-132">Return value</span></span>
>>>>>>> <span data-ttu-id="c7df2-133">образец</span><span class="sxs-lookup"><span data-stu-id="c7df2-133">master</span></span>

<span data-ttu-id="c7df2-134">База данных</span><span class="sxs-lookup"><span data-stu-id="c7df2-134">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="c7df2-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7df2-135">Remarks</span></span>

<span data-ttu-id="c7df2-136">Можно использовать следующие значения для аргумента options.</span><span class="sxs-lookup"><span data-stu-id="c7df2-136">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7df2-137">Параметр</span><span class="sxs-lookup"><span data-stu-id="c7df2-137">Setting</span></span></p></th>
<th><p><span data-ttu-id="c7df2-138">Описание</span><span class="sxs-lookup"><span data-stu-id="c7df2-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7df2-139"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="c7df2-139"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="c7df2-140">Открывает базу данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="c7df2-140">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7df2-141"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="c7df2-141"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="c7df2-142">(По умолчанию) Открывает базу данных в режиме общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c7df2-142">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7df2-143">При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="c7df2-143">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="c7df2-144">Некоторые соображения при использовании dbname.</span><span class="sxs-lookup"><span data-stu-id="c7df2-144">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="c7df2-145">Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7df2-145">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="c7df2-146">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7df2-146">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="c7df2-147">Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="c7df2-147">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="c7df2-148">Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.</span><span class="sxs-lookup"><span data-stu-id="c7df2-148">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <span data-ttu-id="c7df2-149">При получении доступа к Microsoft Access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта **базы данных** , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов [TableDef](tabledef-object-dao.md) в определенных в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="c7df2-149">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


