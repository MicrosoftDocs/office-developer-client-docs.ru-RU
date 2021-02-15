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
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="49cbd-102">Макрокоманда CopyDatabaseFile</span><span class="sxs-lookup"><span data-stu-id="49cbd-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="49cbd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49cbd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49cbd-104">С помощью действия **CopyDatabaseFile** можно сделать копию текущей базы данных Microsoft SQL Server 7.0 или более поздней, подключенной к проекту Access.</span><span class="sxs-lookup"><span data-stu-id="49cbd-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="49cbd-105">Access отсоединит текущую базу данных и прикрепит ее к серверу назначения.</span><span class="sxs-lookup"><span data-stu-id="49cbd-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="49cbd-106">Дополнительные сведения об отсоединение и присоединении базы данных см. в SQL Server документации.</span><span class="sxs-lookup"><span data-stu-id="49cbd-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="49cbd-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="49cbd-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="49cbd-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="49cbd-108">Setting</span></span>

<span data-ttu-id="49cbd-109">Действие **CopyDatabaseFile** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="49cbd-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49cbd-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="49cbd-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="49cbd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="49cbd-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49cbd-112"><strong>Имя файла базы данных</strong></span><span class="sxs-lookup"><span data-stu-id="49cbd-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="49cbd-113">Имя нового файла master Data.</span><span class="sxs-lookup"><span data-stu-id="49cbd-113">The name of the new Master Data File.</span></span> <span data-ttu-id="49cbd-114">Путь к файлу по умолчанию — текущее расположение файла проекта Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="49cbd-114">The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49cbd-115"><strong>Переоценка существующего файла</strong></span><span class="sxs-lookup"><span data-stu-id="49cbd-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="49cbd-116">Указывает, следует ли заменить существующий файл тем же именем.</span><span class="sxs-lookup"><span data-stu-id="49cbd-116">Specifies whether or not to replace an existing file with the same name.</span></span> <span data-ttu-id="49cbd-117">Если за <strong>установлено "Да"</strong> и имя файла уже существует, файл перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="49cbd-117">If set to <strong>Yes</strong> and the filename already exists, the file is overwritten.</span></span> <span data-ttu-id="49cbd-118">Если за <strong>установлено "Нет"</strong> и имя файла уже существует, файл не перезаписывается и действие не происходит.</span><span class="sxs-lookup"><span data-stu-id="49cbd-118">If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails.</span></span> <span data-ttu-id="49cbd-119">Если файл еще не существует, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="49cbd-119">If the file does not already exist, this setting is ignored.</span></span> <span data-ttu-id="49cbd-120">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="49cbd-120">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49cbd-121"><strong>Отключение всех пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="49cbd-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="49cbd-122">Указывает, должен ли Access принудительно отключать пользователей от базы данных.</span><span class="sxs-lookup"><span data-stu-id="49cbd-122">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="49cbd-123">Если за <strong>установлено "Да",</strong>все пользователи, подключенные к текущей базе данных, отключаются, чтобы операция копирования базы данных продолжалась.</span><span class="sxs-lookup"><span data-stu-id="49cbd-123">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="49cbd-124">Если установлено <strong>"Нет"</strong> и к базе данных подключен один или несколько пользователей, операция копирования базы данных не будет удаться.</span><span class="sxs-lookup"><span data-stu-id="49cbd-124">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="49cbd-125">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="49cbd-125">The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="49cbd-126"><strong>ПРЕДУПРЕЖДЕНИЕ.</strong>Отключение пользователей от базы данных без соответствующего предупреждения может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="49cbd-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="49cbd-127">Заметки</span><span class="sxs-lookup"><span data-stu-id="49cbd-127">Remarks</span></span>

<span data-ttu-id="49cbd-128">Операция копирования является синхронной, поэтому вы не сможете выполнять другие операции, пока копия базы данных не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="49cbd-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="49cbd-129">Действие **CopyDatabaseFile** не только копирует данные, определения данных и объекты базы данных, но также копирует расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значения поиска.</span><span class="sxs-lookup"><span data-stu-id="49cbd-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="49cbd-130">Требования для копирования базы данных:</span><span class="sxs-lookup"><span data-stu-id="49cbd-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="49cbd-131">Перед копированием файла базы данных необходимо отключить все приложения и пользователей.</span><span class="sxs-lookup"><span data-stu-id="49cbd-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="49cbd-132">Все объекты и представления, кроме области навигации, должны быть закрыты.</span><span class="sxs-lookup"><span data-stu-id="49cbd-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="49cbd-133">Текущая база данных не должна быть реплицирована.</span><span class="sxs-lookup"><span data-stu-id="49cbd-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="49cbd-134">Исходная база данных сервера должна быть Microsoft SQL Server версии 7.0 или более поздней или SQL Server 2000 Desktop Engine, запущенной на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="49cbd-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="49cbd-135">Базой SQL Server на сервере-источнике должна быть одна файловая база данных.</span><span class="sxs-lookup"><span data-stu-id="49cbd-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="49cbd-136">Необходимо быть членом роли sysadmin на компьютерах источника и назначения SQL Server компьютерах.</span><span class="sxs-lookup"><span data-stu-id="49cbd-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="49cbd-137">Чтобы запустить действие **CopyDatabaseFile** в модуле Visual Basic для приложений, используйте метод **CopyDatabaseFile** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="49cbd-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

