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
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="23e6f-102">Макрокоманда CopyDatabaseFile</span><span class="sxs-lookup"><span data-stu-id="23e6f-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="23e6f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23e6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23e6f-104">Вы можете использовать действие **копидатабасефиле** , чтобы создать копию текущей базы данных Microsoft SQL Server 7,0 или более поздней версии, подключенной к проекту Access.</span><span class="sxs-lookup"><span data-stu-id="23e6f-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="23e6f-105">Access отсоединяет текущую базу данных, а затем подключает ее к конечному серверу.</span><span class="sxs-lookup"><span data-stu-id="23e6f-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="23e6f-106">Дополнительные сведения об отсоединении и присоединении базы данных содержатся в документации по SQL Server.</span><span class="sxs-lookup"><span data-stu-id="23e6f-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="23e6f-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="23e6f-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="23e6f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23e6f-108">Setting</span></span>

<span data-ttu-id="23e6f-109">Макрокоманда **копидатабасефиле** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="23e6f-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23e6f-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="23e6f-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="23e6f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="23e6f-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23e6f-112"><strong>Имя файла базы данных</strong></span><span class="sxs-lookup"><span data-stu-id="23e6f-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="23e6f-113">Имя нового файла основных данных.</span><span class="sxs-lookup"><span data-stu-id="23e6f-113">The name of the new Master Data File.</span></span> <span data-ttu-id="23e6f-114">Путь по умолчанию для файла — это текущее расположение файла проекта Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="23e6f-114">The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23e6f-115"><strong>Перезаписать существующий файл</strong></span><span class="sxs-lookup"><span data-stu-id="23e6f-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="23e6f-116">Указывает, следует ли заменить существующий файл с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="23e6f-116">Specifies whether or not to replace an existing file with the same name.</span></span> <span data-ttu-id="23e6f-117">Если задано значение <strong>"Да"</strong> , а имя файла уже существует, файл перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="23e6f-117">If set to <strong>Yes</strong> and the filename already exists, the file is overwritten.</span></span> <span data-ttu-id="23e6f-118">Если задано значение " <strong>нет</strong> ", а имя файла уже существует, файл не перезаписывается и действие не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23e6f-118">If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails.</span></span> <span data-ttu-id="23e6f-119">Если файл еще не существует, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="23e6f-119">If the file does not already exist, this setting is ignored.</span></span> <span data-ttu-id="23e6f-120">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="23e6f-120">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23e6f-121"><strong>Отключение всех пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="23e6f-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="23e6f-122">Указывает, следует ли запретить пользователям получать доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="23e6f-122">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="23e6f-123">Если задано значение <strong>"Да"</strong>, все пользователи, подключенные к текущей базе данных, будут отключены, чтобы можно было продолжить операцию копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="23e6f-123">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="23e6f-124">Если для параметра установлено значение <strong>нет</strong> и один или несколько пользователей подключены к базе данных, операция копирования базы данных завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="23e6f-124">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="23e6f-125">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="23e6f-125">The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="23e6f-126"><strong>Предупреждение</strong>: Отключение пользователей от базы данных без соответствующего предупреждения может приводить к потере данных.</span><span class="sxs-lookup"><span data-stu-id="23e6f-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="23e6f-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="23e6f-127">Remarks</span></span>

<span data-ttu-id="23e6f-128">Операция копирования синхронна, поэтому невозможно выполнить другие операции, пока копия базы данных не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="23e6f-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="23e6f-129">Действие **копидатабасефиле** не только копирует данные, определения данных и объекты базы данных, но и копирует расширенные свойства, такие как значения по умолчанию, ограничения текста и значения подстановки.</span><span class="sxs-lookup"><span data-stu-id="23e6f-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="23e6f-130">Требования для копирования базы данных:</span><span class="sxs-lookup"><span data-stu-id="23e6f-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="23e6f-131">Перед копированием файла базы данных необходимо отключить всех приложений и пользователей.</span><span class="sxs-lookup"><span data-stu-id="23e6f-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="23e6f-132">Все объекты и представления, кроме области навигации, должны быть закрыты.</span><span class="sxs-lookup"><span data-stu-id="23e6f-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="23e6f-133">Текущая база данных не должна быть реплицирована.</span><span class="sxs-lookup"><span data-stu-id="23e6f-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="23e6f-134">База данных исходного сервера должна иметь Microsoft SQL Server версии 7,0 или более поздней версии или SQL Server 2000 Desktop Engine, запущенный на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="23e6f-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="23e6f-135">База данных SQL Server на исходном сервере должна быть одной базой данных файлов.</span><span class="sxs-lookup"><span data-stu-id="23e6f-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="23e6f-136">Необходимо быть членом роли sysadmin как на исходном, так и на целевом компьютере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="23e6f-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="23e6f-137">Чтобы запустить действие **копидатабасефиле** в модуле Visual Basic для приложений, используйте метод **копидатабасефиле** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="23e6f-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

