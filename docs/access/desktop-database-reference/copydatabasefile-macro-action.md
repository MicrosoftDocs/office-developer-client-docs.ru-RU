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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699445"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="14c2c-102">Макрокоманда CopyDatabaseFile</span><span class="sxs-lookup"><span data-stu-id="14c2c-102">CopyDatabaseFile macro action</span></span>

<span data-ttu-id="14c2c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14c2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14c2c-104">**КопироватьФайлБазыДанных** можно использовать для создания копии текущего Microsoft SQL Server 7.0 или более поздняя версия базы данных, подключенные к проект Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="14c2c-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="14c2c-105">Access отключает текущую базу данных и подключает ее к конечному серверу.</span><span class="sxs-lookup"><span data-stu-id="14c2c-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="14c2c-106">Дополнительные сведения о присоединение и отсоединение базы данных SQL Server см.</span><span class="sxs-lookup"><span data-stu-id="14c2c-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="14c2c-107">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="14c2c-107">This action will not be allowed if the database is not trusted.</span></span> 


## <a name="setting"></a><span data-ttu-id="14c2c-108">Setting</span><span class="sxs-lookup"><span data-stu-id="14c2c-108">Setting</span></span>

<span data-ttu-id="14c2c-109">**КопироватьФайлБазыДанных** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="14c2c-109">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14c2c-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="14c2c-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="14c2c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="14c2c-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14c2c-112"><strong>Имя файла базы данных</strong></span><span class="sxs-lookup"><span data-stu-id="14c2c-112"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="14c2c-113">Имя нового файла данных образец.</span><span class="sxs-lookup"><span data-stu-id="14c2c-113">The name of the new Master Data File.</span></span> <span data-ttu-id="14c2c-114">Путь по умолчанию является текущее расположение файла проекта Microsoft Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="14c2c-114">The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14c2c-115"><strong>Перезапись существующего файла</strong></span><span class="sxs-lookup"><span data-stu-id="14c2c-115"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="14c2c-116">Указывает, следует ли заменить существующий файл с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="14c2c-116">Specifies whether or not to replace an existing file with the same name.</span></span> <span data-ttu-id="14c2c-117">Если значение <strong>Да</strong> и имя файла уже существует, файл перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="14c2c-117">If set to <strong>Yes</strong> and the filename already exists, the file is overwritten.</span></span> <span data-ttu-id="14c2c-118">Если значение <strong>Нет</strong> и имя файла уже существует, файл не перезаписывается и не удается выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="14c2c-118">If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails.</span></span> <span data-ttu-id="14c2c-119">Если файл еще не существует, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="14c2c-119">If the file does not already exist, this setting is ignored.</span></span> <span data-ttu-id="14c2c-120">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="14c2c-120">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14c2c-121"><strong>Отключите всех пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="14c2c-121"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="14c2c-122">Указывает, следует ли доступа принудительное отключение базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="14c2c-122">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="14c2c-123">Если параметр имеет значение <strong>Yes</strong>, все пользователи, подключенные к текущей базе данных не соединены по сети, чтобы операции копирования базы данных можно продолжить.</span><span class="sxs-lookup"><span data-stu-id="14c2c-123">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="14c2c-124">Если значение <strong>No</strong> , а один или несколько пользователей подключены к базе данных, возникает ошибка операции копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="14c2c-124">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="14c2c-125">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="14c2c-125">The default is <strong>No</strong>.</span></span></p><p><span data-ttu-id="14c2c-126"><strong>Предупреждение</strong>: отключение пользователей из базы данных без предварительного предупреждения может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="14c2c-126"><strong>WARNING</strong>: Disconnecting users from a database without adequate warning can lead to data loss.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="14c2c-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="14c2c-127">Remarks</span></span>

<span data-ttu-id="14c2c-128">Операция копирования является синхронным, поэтому не могут выполнять другие операции до завершения копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="14c2c-128">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="14c2c-129">**КопироватьФайлБазыДанных** не только копирование данных, определений данных и объектов базы данных, но также копирует расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значений подстановки.</span><span class="sxs-lookup"><span data-stu-id="14c2c-129">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="14c2c-130">Требования для копирования базы данных:</span><span class="sxs-lookup"><span data-stu-id="14c2c-130">Requirements for copying a database:</span></span>

- <span data-ttu-id="14c2c-131">Перед копированием файла базы данных, необходимо отключить все приложения и пользователи.</span><span class="sxs-lookup"><span data-stu-id="14c2c-131">You must disconnect all applications and users before you copy the database file.</span></span>

- <span data-ttu-id="14c2c-132">Необходимо закрыть все объекты и представлений, за исключением области навигации.</span><span class="sxs-lookup"><span data-stu-id="14c2c-132">All objects and views except the Navigation Pane must be closed.</span></span>

- <span data-ttu-id="14c2c-133">Текущей базы данных не должна быть реплицирована.</span><span class="sxs-lookup"><span data-stu-id="14c2c-133">The current database must not be replicated.</span></span>

- <span data-ttu-id="14c2c-134">Базы данных-источника сервера должны быть Microsoft SQL Server версии 7.0 или более поздней версии или SQL Server 2000 Desktop Engine на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="14c2c-134">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

- <span data-ttu-id="14c2c-135">База данных SQL Server на исходном сервере должен быть один файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="14c2c-135">The SQL Server database on the source server must be a single file database.</span></span>

- <span data-ttu-id="14c2c-136">Необходимо быть членом роли sysadmin на исходном и целевом компьютерах SQL Server.</span><span class="sxs-lookup"><span data-stu-id="14c2c-136">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="14c2c-137">Чтобы запустить **КопироватьФайлБазыДанных** в Visual Basic для приложений модуль, используйте метод **CopyDatabaseFile** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="14c2c-137">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

