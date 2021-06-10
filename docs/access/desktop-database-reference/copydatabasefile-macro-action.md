---
title: Макрокоманда CopyDatabaseFile
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3c98d8795bb7039c0ae158414401dc5d754066f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295501"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="34230-102">Макрокоманда CopyDatabaseFile</span><span class="sxs-lookup"><span data-stu-id="34230-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="34230-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34230-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34230-104">Вы можете использовать **действие CopyDatabaseFile,** чтобы сделать копию текущей Microsoft SQL Server 7.0 или более поздней базы данных, подключенной к проекту Access.</span><span class="sxs-lookup"><span data-stu-id="34230-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="34230-105">Access отсоединит текущую базу данных и прикрепит ее к серверу назначения.</span><span class="sxs-lookup"><span data-stu-id="34230-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="34230-106">Дополнительные сведения об отсоединения и присоединении базы данных см. в SQL Server документации.</span><span class="sxs-lookup"><span data-stu-id="34230-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="34230-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="34230-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="34230-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="34230-108">Setting</span></span>

<span data-ttu-id="34230-109">Действие **CopyDatabaseFile** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="34230-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34230-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="34230-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="34230-111">Описание</span><span class="sxs-lookup"><span data-stu-id="34230-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34230-112"><strong>Имя файла базы данных</strong></span><span class="sxs-lookup"><span data-stu-id="34230-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="34230-113">Имя нового файла мастер-данных.</span><span class="sxs-lookup"><span data-stu-id="34230-113">The name of the new Master Data File.</span></span> <span data-ttu-id="34230-114">Путь по умолчанию для файла — текущее расположение файла проекта Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="34230-114">The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34230-115"><strong>Переописывание существующего файла</strong></span><span class="sxs-lookup"><span data-stu-id="34230-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="34230-116">Указывает, следует ли заменить существующий файл с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="34230-116">Specifies whether or not to replace an existing file with the same name.</span></span> <span data-ttu-id="34230-117">Если <strong>установлено да,</strong> и имя файла уже существует, файл перезаписан.</span><span class="sxs-lookup"><span data-stu-id="34230-117">If set to <strong>Yes</strong> and the filename already exists, the file is overwritten.</span></span> <span data-ttu-id="34230-118">Если <strong>установлено нет</strong> и имя файла уже существует, файл не перезаписывается и действие не удается.</span><span class="sxs-lookup"><span data-stu-id="34230-118">If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails.</span></span> <span data-ttu-id="34230-119">Если файл еще не существует, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="34230-119">If the file does not already exist, this setting is ignored.</span></span> <span data-ttu-id="34230-120">По умолчанию — <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="34230-120">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34230-121"><strong>Отключение всех пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="34230-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="34230-122">Указывает, должен ли Access выговарить пользователей из базы данных.</span><span class="sxs-lookup"><span data-stu-id="34230-122">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="34230-123">Если <strong>установлено да,</strong>все пользователи, подключенные к текущей базе данных, отключаются, чтобы операция базы данных копирования продолжалась.</span><span class="sxs-lookup"><span data-stu-id="34230-123">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="34230-124">Если <strong>установлено, что нет</strong> и один или несколько пользователей подключены к базе данных, операция базы данных копирования сбой.</span><span class="sxs-lookup"><span data-stu-id="34230-124">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="34230-125">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="34230-125">The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="34230-126"><strong>ВНИМАНИЕ.</strong>Отключение пользователей из базы данных без надлежащего предупреждения может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="34230-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="34230-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="34230-127">Remarks</span></span>

<span data-ttu-id="34230-128">Операция копирования синхронна, поэтому другие операции нельзя выполнять до завершения копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="34230-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="34230-129">Действие **CopyDatabaseFile** не только копирует данные, определения данных и объекты баз данных, но и копирует расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значения поиска.</span><span class="sxs-lookup"><span data-stu-id="34230-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="34230-130">Требования к копированию базы данных:</span><span class="sxs-lookup"><span data-stu-id="34230-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="34230-131">Перед копированием файла базы данных необходимо отключить все приложения и пользователей.</span><span class="sxs-lookup"><span data-stu-id="34230-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="34230-132">Все объекты и представления, кроме области навигации, должны быть закрыты.</span><span class="sxs-lookup"><span data-stu-id="34230-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="34230-133">Текущая база данных не должна реплицироваться.</span><span class="sxs-lookup"><span data-stu-id="34230-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="34230-134">База данных исходных серверов должна быть Microsoft SQL Server версии 7.0 или более поздней версии или SQL Server 2000 desktop Engine, запущенной на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="34230-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="34230-135">Базой SQL Server на сервере исходных данных должна быть единая база данных файлов.</span><span class="sxs-lookup"><span data-stu-id="34230-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="34230-136">Вы должны быть членом роли sysadmin на исходных и SQL Server компьютерах.</span><span class="sxs-lookup"><span data-stu-id="34230-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="34230-137">Чтобы выполнить **действие CopyDatabaseFile** в Visual Basic для приложений, используйте метод **CopyDatabaseFile** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="34230-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

