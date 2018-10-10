---
title: CopyDatabaseFile Macro Action
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b52644cb9a0a5140f45c42eaead84a63723c23e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482737"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="3adba-102">CopyDatabaseFile Macro Action</span><span class="sxs-lookup"><span data-stu-id="3adba-102">CopyDatabaseFile Macro Action</span></span>


<span data-ttu-id="3adba-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3adba-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3adba-104">**КопироватьФайлБазыДанных** можно использовать для создания копии текущего Microsoft SQL Server 7.0 или более поздняя версия базы данных, подключенные к проект Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3adba-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="3adba-105">Access отключает текущую базу данных и подключает ее к конечному серверу.</span><span class="sxs-lookup"><span data-stu-id="3adba-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="3adba-106">Дополнительные сведения о присоединение и отсоединение базы данных SQL Server см.</span><span class="sxs-lookup"><span data-stu-id="3adba-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3adba-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="3adba-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="3adba-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="3adba-109">Setting</span></span>

<span data-ttu-id="3adba-110">**КопироватьФайлБазыДанных** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="3adba-110">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3adba-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3adba-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3adba-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3adba-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3adba-113"><strong>Имя файла базы данных</strong></span><span class="sxs-lookup"><span data-stu-id="3adba-113"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3adba-114">Имя нового файла данных образец.</span><span class="sxs-lookup"><span data-stu-id="3adba-114">The name of the new Master Data File.</span></span> <span data-ttu-id="3adba-115">Путь по умолчанию является текущее расположение файла проекта Microsoft Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="3adba-115">The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3adba-116"><strong>Перезапись существующего файла</strong></span><span class="sxs-lookup"><span data-stu-id="3adba-116"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="3adba-117">Указывает, следует ли заменить существующий файл с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="3adba-117">Specifies whether or not to replace an existing file with the same name.</span></span> <span data-ttu-id="3adba-118">Если значение <strong>Да</strong> и имя файла уже существует, файл перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="3adba-118">If set to <strong>Yes</strong> and the filename already exists, the file is overwritten.</span></span> <span data-ttu-id="3adba-119">Если значение <strong>Нет</strong> и имя файла уже существует, файл не перезаписывается и не удается выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="3adba-119">If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails.</span></span> <span data-ttu-id="3adba-120">Если файл еще не существует, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3adba-120">If the file does not already exist, this setting is ignored.</span></span> <span data-ttu-id="3adba-121">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="3adba-121">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3adba-122"><strong>Отключите всех пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="3adba-122"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="3adba-123">Указывает, следует ли доступа принудительное отключение базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3adba-123">Specifies whether or not Access should force users off the database.</span></span> <span data-ttu-id="3adba-124">Если параметр имеет значение <strong>Yes</strong>, все пользователи, подключенные к текущей базе данных не соединены по сети, чтобы операции копирования базы данных можно продолжить.</span><span class="sxs-lookup"><span data-stu-id="3adba-124">If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed.</span></span> <span data-ttu-id="3adba-125">Если значение <strong>No</strong> , а один или несколько пользователей подключены к базе данных, возникает ошибка операции копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="3adba-125">If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails.</span></span> <span data-ttu-id="3adba-126">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="3adba-126">The default is <strong>No</strong>.</span></span></p>

> [!WARNING]
> <P><span data-ttu-id="3adba-127">Отключение пользователей из базы данных без предварительного предупреждения может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="3adba-127">Disconnecting users from a database without adequate warning can lead to data loss.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3adba-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="3adba-128">Remarks</span></span>

<span data-ttu-id="3adba-129">Операция копирования является синхронным, поэтому не могут выполнять другие операции до завершения копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="3adba-129">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="3adba-130">**КопироватьФайлБазыДанных** не только копирование данных, определений данных и объектов базы данных, но также копирует расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значений подстановки.</span><span class="sxs-lookup"><span data-stu-id="3adba-130">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="3adba-131">Требования для копирования базы данных:</span><span class="sxs-lookup"><span data-stu-id="3adba-131">Requirements for copying a database:</span></span>

  - <span data-ttu-id="3adba-132">Перед копированием файла базы данных, необходимо отключить все приложения и пользователи.</span><span class="sxs-lookup"><span data-stu-id="3adba-132">You must disconnect all applications and users before you copy the database file.</span></span>

  - <span data-ttu-id="3adba-133">Необходимо закрыть все объекты и представлений, за исключением области навигации.</span><span class="sxs-lookup"><span data-stu-id="3adba-133">All objects and views except the Navigation Pane must be closed.</span></span>

  - <span data-ttu-id="3adba-134">Текущей базы данных не должна быть реплицирована.</span><span class="sxs-lookup"><span data-stu-id="3adba-134">The current database must not be replicated.</span></span>

  - <span data-ttu-id="3adba-135">Базы данных-источника сервера должны быть Microsoft SQL Server версии 7.0 или более поздней версии или SQL Server 2000 Desktop Engine на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3adba-135">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="3adba-136">База данных SQL Server на исходном сервере должен быть один файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="3adba-136">The SQL Server database on the source server must be a single file database.</span></span>

  - <span data-ttu-id="3adba-137">Необходимо быть членом роли sysadmin на исходном и целевом компьютерах SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3adba-137">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="3adba-138">Чтобы запустить **КопироватьФайлБазыДанных** в Visual Basic для приложений модуль, используйте метод **CopyDatabaseFile** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="3adba-138">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

