---
title: Обеспечение наличия достаточного места в TempDB
TOCTitle: Ensuring sufficient TempDB space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6414c9dd4c3218c2c2bf90f39d0cfb950e6e1018
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293576"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="6ae58-102">Обеспечение наличия достаточного места в TempDB</span><span class="sxs-lookup"><span data-stu-id="6ae58-102">Ensuring sufficient TempDB space</span></span>


<span data-ttu-id="6ae58-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ae58-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ae58-104">Если при обработке объектов Recordset, для обработки объектов [recordset,](recordset-object-ado.md) для обработки Microsoft SQL Server 6,5, могут возникнуть ошибки, может потребоваться увеличить размер TempDB.</span><span class="sxs-lookup"><span data-stu-id="6ae58-104">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB.</span></span> <span data-ttu-id="6ae58-105">(Для некоторых запросов требуется временное пространство обработки; например, для запроса с предложением ORDER BY требуется определенный набор записей, для которого требуется некоторое временное пространство.)</span><span class="sxs-lookup"><span data-stu-id="6ae58-105">(Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ae58-106">Прочитайте эту процедуру перед выполнением действий, так как сжать устройство после его расширения не так просто.</span><span class="sxs-lookup"><span data-stu-id="6ae58-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="6ae58-107">По умолчанию в Microsoft SQL Server 7.0 и более поздних, tempDB автоматически растет по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6ae58-107">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed.</span></span> <span data-ttu-id="6ae58-108">Следовательно, эта процедура может потребоваться только на серверах с более ранними версиями, чем 7.0.</span><span class="sxs-lookup"><span data-stu-id="6ae58-108">Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="6ae58-109">**Увеличение пространства TempDB на SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="6ae58-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="6ae58-110">Запустите Microsoft SQL Server Enterprise Manager, откройте дерево сервера, а затем откройте дерево "Устройства базы данных".</span><span class="sxs-lookup"><span data-stu-id="6ae58-110">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="6ae58-111">Выберите (физическое) устройство для расширения, например "Мастер", и  дважды щелкните устройство, чтобы открыть диалоговое окно "Изменение устройства базы данных".</span><span class="sxs-lookup"><span data-stu-id="6ae58-111">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box.</span></span> <span data-ttu-id="6ae58-112">В этом диалоговом окне показано, сколько места используется текущими базами данных.</span><span class="sxs-lookup"><span data-stu-id="6ae58-112">This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="6ae58-113">В поле **"Размер"** увеличите устройство до нужного объема (например, 50 мегабайт (МБ) места на жестком диске).</span><span class="sxs-lookup"><span data-stu-id="6ae58-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="6ae58-114">Нажмите **кнопку "Изменить",** чтобы увеличить объем пространства, до которого может развернуться (логический) TempDB.</span><span class="sxs-lookup"><span data-stu-id="6ae58-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="6ae58-115">Откройте дерево баз данных на сервере и дважды щелкните  **TempDB,** чтобы открыть диалоговое окно "Изменение базы данных".</span><span class="sxs-lookup"><span data-stu-id="6ae58-115">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box.</span></span> <span data-ttu-id="6ae58-116">На **вкладке "База** данных" указан объем пространства, выделенного для TempDB **(размер данных).**</span><span class="sxs-lookup"><span data-stu-id="6ae58-116">The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**).</span></span> <span data-ttu-id="6ae58-117">По умолчанию это 2 МБ.</span><span class="sxs-lookup"><span data-stu-id="6ae58-117">By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="6ae58-118">В группе **"Размер"** нажмите кнопку **"Развернуть".**</span><span class="sxs-lookup"><span data-stu-id="6ae58-118">Under the **Size** group, click **Expand**.</span></span> <span data-ttu-id="6ae58-119">На графиках покажите доступное и выделенное пространство на каждом физическом устройстве.</span><span class="sxs-lookup"><span data-stu-id="6ae58-119">The graphs show the available and allocated space on each of the physical devices.</span></span> <span data-ttu-id="6ae58-120">Полосы в цвете маруна представляют доступное пространство.</span><span class="sxs-lookup"><span data-stu-id="6ae58-120">The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="6ae58-121">Выберите устройство **журнала,** например "Хозяин", чтобы отобразить доступный размер в поле **"Размер ( МБ)".**</span><span class="sxs-lookup"><span data-stu-id="6ae58-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="6ae58-122">Нажмите **кнопку "Развернуть сейчас",** чтобы выделить это пространство для базы данных TempDB.</span><span class="sxs-lookup"><span data-stu-id="6ae58-122">Click **Expand Now** to allocate that space to the TempDB database.</span></span> <span data-ttu-id="6ae58-123">В **диалоговом** окне "Изменение базы данных" отображается новый выделенный размер для TempDB.</span><span class="sxs-lookup"><span data-stu-id="6ae58-123">The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="6ae58-124">Дополнительные сведения об этой теме можно найти в Microsoft SQL Server справки enterprise Manager по запросу "Диалоговое окно "Развернуть базу данных".</span><span class="sxs-lookup"><span data-stu-id="6ae58-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

