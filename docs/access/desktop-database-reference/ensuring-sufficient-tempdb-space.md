---
title: Обеспечение наличия достаточного места в TempDB
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d049a098a7f7cfd826c6c5945c71831acbceb04
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863054"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="0e9ea-102">Обеспечение наличия достаточного места в TempDB</span><span class="sxs-lookup"><span data-stu-id="0e9ea-102">Ensuring Sufficient TempDB Space</span></span>


<span data-ttu-id="0e9ea-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e9ea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0e9ea-104">При возникновении ошибок во время обработки объектов [наборов записей](recordset-object-ado.md) , которые должны обработки места на Microsoft SQL Server 6.5, может потребоваться увеличение размера базы данных TempDB.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-104">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB.</span></span> <span data-ttu-id="0e9ea-105">(Некоторые запросы требуют пространства временные обработки; например запрос с предложение ORDER BY требует сортировку набора **записей**, что требует временного место).</span><span class="sxs-lookup"><span data-stu-id="0e9ea-105">(Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e9ea-106">Прочитайте эту процедуру перед выполнением действий, так как он не так просто уменьшения размера устройства, когда она развернута.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="0e9ea-107">По умолчанию в Microsoft SQL Server 7.0 и более поздних версий базы данных TempDB присваивается автоматически увеличиваться по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-107">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed.</span></span> <span data-ttu-id="0e9ea-108">Таким образом эта процедура может быть только необходимые на серверах под управлением версии меньше 7.0.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-108">Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="0e9ea-109">**Чтобы увеличить размер базы данных TempDB на SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="0e9ea-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="0e9ea-110">Запустите Microsoft® SQL Server Enterprise Manager Открытие дерева для сервера и откройте дерево устройств базы данных.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-110">Start Microsoft® SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="0e9ea-111">Выберите устройство (физических) для развертывания, такие как главные и дважды щелкните устройство, чтобы открыть диалоговое окно **Изменение устройства базы данных** .</span><span class="sxs-lookup"><span data-stu-id="0e9ea-111">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box.</span></span> <span data-ttu-id="0e9ea-112">Это диалоговое окно показывает объем пространства, используя текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-112">This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="0e9ea-113">В поле **размер** увеличение устройства требуемое число (например, 50 мегабайт (МБ) пространства жесткого диска).</span><span class="sxs-lookup"><span data-stu-id="0e9ea-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="0e9ea-114">Нажмите кнопку **Изменить сейчас** , чтобы увеличить объем пространства, к которому можно развернуть (логическое) базы данных TempDB.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="0e9ea-115">Открытие дерева баз данных на сервере и затем дважды щелкните значок **базы данных TempDB** , чтобы открыть диалоговое окно **Изменение базы данных** .</span><span class="sxs-lookup"><span data-stu-id="0e9ea-115">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box.</span></span> <span data-ttu-id="0e9ea-116">На вкладке **базы данных** перечислены дискового пространства, выделенный в текущий момент для базы данных TempDB (**Размер данных**).</span><span class="sxs-lookup"><span data-stu-id="0e9ea-116">The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**).</span></span> <span data-ttu-id="0e9ea-117">По умолчанию это 2 МБ.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-117">By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="0e9ea-118">В разделе **размер** группы нажмите кнопку **Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-118">Under the **Size** group, click **Expand**.</span></span> <span data-ttu-id="0e9ea-119">На графиках показано доступны и выделенного места на каждом из физических устройств.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-119">The graphs show the available and allocated space on each of the physical devices.</span></span> <span data-ttu-id="0e9ea-120">Столбцы в Темно-бордовая цвета представляют доступное место.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-120">The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="0e9ea-121">Выберите **Журнала устройств**, такие как главные, чтобы отобразить доступные размер в поле **Размер (МБ)** .</span><span class="sxs-lookup"><span data-stu-id="0e9ea-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="0e9ea-122">Нажмите кнопку **Развернуть теперь** распределения этого пространства для базы данных TempDB.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-122">Click **Expand Now** to allocate that space to the TempDB database.</span></span> <span data-ttu-id="0e9ea-123">Диалоговое окно **Изменение базы данных** отображаются новые выделенный размер для базы данных TempDB.</span><span class="sxs-lookup"><span data-stu-id="0e9ea-123">The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="0e9ea-124">Дополнительные сведения по этому разделу найти в файле справки Microsoft SQL Server Enterprise Manager «Развернуть диалоговое окно базы данных.»</span><span class="sxs-lookup"><span data-stu-id="0e9ea-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

