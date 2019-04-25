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
localization_priority: Priority
ms.openlocfilehash: 1cd4188931999284a6454064a0906b64cf1f519a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294255"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="e9f6f-102">Метод DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9f6f-102">DBEngine.OpenDatabase Method (DAO)</span></span>

<span data-ttu-id="e9f6f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9f6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9f6f-104">Открывает указанную базу данных и возвращает ссылку на объект **[Database](database-object-dao.md)**, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-104">Opens a specified database in a Workspace object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f6f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9f6f-105">Syntax</span></span>

<span data-ttu-id="e9f6f-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="e9f6f-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="e9f6f-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-107">*expression* A variable that represents a **Range** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9f6f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9f6f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9f6f-109">Имя</span><span class="sxs-lookup"><span data-stu-id="e9f6f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e9f6f-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="e9f6f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e9f6f-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e9f6f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e9f6f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e9f6f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9f6f-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="e9f6f-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9f6f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e9f6f-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e9f6f-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-116">Имя существующего файла базы данных Microsoft Access или имя источника данных (DSN) для источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-116">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source.</span></span> <span data-ttu-id="e9f6f-117">См. свойство <strong> <a href="connection-name-property-dao.md">Name</a> </strong> для получения дополнительной информации о настройке данного значения.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f6f-118"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="e9f6f-118"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-119">Необязательно</span><span class="sxs-lookup"><span data-stu-id="e9f6f-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="e9f6f-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e9f6f-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-121">Определяет различные опции для базы данных, согласно данным в Комментариях.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9f6f-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="e9f6f-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-123">Необязательно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="e9f6f-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e9f6f-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-125">Установите значение <strong>True</strong>, если вы хотите открыть базу данных с правами доступа только для чтения, или <strong>False</strong> (установлено по умолчанию), если вы хотите открыть базу данных с правами доступа на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f6f-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="e9f6f-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-127">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="e9f6f-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e9f6f-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-129">Определяет различные сведения о подключении, включая пароли.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="e9f6f-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9f6f-130">Return value</span></span>

<span data-ttu-id="e9f6f-131">База данных</span><span class="sxs-lookup"><span data-stu-id="e9f6f-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f6f-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9f6f-132">Remarks</span></span>

<span data-ttu-id="e9f6f-133">Вы можете использовать следующие значения для аргумента Options.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9f6f-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="e9f6f-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="e9f6f-135">Описание</span><span class="sxs-lookup"><span data-stu-id="e9f6f-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9f6f-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="e9f6f-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-137">Открытие базы данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9f6f-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="e9f6f-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="e9f6f-139">(По умолчанию) Открытие базы данных в режиме совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9f6f-140">Когда вы открываете базу данных, она автоматически добавляется коллекцию **Databases**.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="e9f6f-141">Несколько советов в отношении применения dbname:</span><span class="sxs-lookup"><span data-stu-id="e9f6f-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="e9f6f-142">Если он ссылается на базу данных, которая уже открыта для доступа другому пользователю, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="e9f6f-143">Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="e9f6f-144">Если он является строкой нулевой длины (""), а для *connect* установлено значение "ODBC;", откроется диалоговое окно со списком всех зарегистрированных имен источник данных ODBC, где пользователь может выбрать базу данных.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="e9f6f-145">Чтобы закрыть базу данных, а значит удалить объект **Database** из коллекции **Databases**, используйте метод **[Close](connection-close-method-dao.md)** для объекта.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="e9f6f-146">При обращении к источнику данных ODBC, подключенного к ядру СУБД Microsoft Access вы можете повысить производительность вашего приложения, открыв объект **Database**, связанный с источником данных ODBC, не прибегая к связыванию отдельных объектов [TableDef](tabledef-object-dao.md) с определенными таблицами источника данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


