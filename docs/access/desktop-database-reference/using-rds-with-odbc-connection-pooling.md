---
title: Using RDS with ODBC Connection Pooling
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312119"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="52681-102">Использование RDS с группировкой подключений ODBC</span><span class="sxs-lookup"><span data-stu-id="52681-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="52681-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52681-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52681-104">При использовании источника данных ODBC можно использовать параметр пула подключений в службах IIS для обеспечения высокой производительности обработки клиентской нагрузки.</span><span class="sxs-lookup"><span data-stu-id="52681-104">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</span></span> <span data-ttu-id="52681-105">Пулы подключений — это диспетчер ресурсов для подключений, который поддерживает открытое состояние для часто используемых подключений.</span><span class="sxs-lookup"><span data-stu-id="52681-105">Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="52681-106">Чтобы включить пул подключений, обратитесь к документации по службам Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="52681-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="52681-107">Обратите внимание, что включение пула подключений может привести к другим ограничениям веб-сервера, как отмечено в Microsoft IIS документации.</span><span class="sxs-lookup"><span data-stu-id="52681-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="52681-108">Чтобы обеспечить стабильность пула подключений и повышение производительности, необходимо настроить Microsoft SQL Server для использования сетевой библиотеки TCP/IP-socket.</span><span class="sxs-lookup"><span data-stu-id="52681-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="52681-109">Для этого необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="52681-109">To do this, you need to:</span></span>

  - <span data-ttu-id="52681-110">Настройте компьютер SQL Server для использования TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="52681-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="52681-111">Настройте веб-сервер для использования TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="52681-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="52681-112">Настройка компьютера SQL Server для использования TCP/IP-sockets</span><span class="sxs-lookup"><span data-stu-id="52681-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="52681-113">На компьютере SQL Server запустите программу установки SQL Server, чтобы взаимодействие с источником данных использовали сетевую библиотеку TCP/IP-socket.</span><span class="sxs-lookup"><span data-stu-id="52681-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="52681-114">**Указание сетевой библиотеки TCP/IP-SQL Server компьютера**</span><span class="sxs-lookup"><span data-stu-id="52681-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="52681-115">**В Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="52681-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="52681-116">В меню **"Пуск"** найдите пункт "Программы", выберите Microsoft SQL Server **6.5,** а затем нажмите кнопку **SQL программы установки.** </span><span class="sxs-lookup"><span data-stu-id="52681-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="52681-117">Дважды **нажмите кнопку** "Продолжить".</span><span class="sxs-lookup"><span data-stu-id="52681-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="52681-118">В **диалоговом окне Microsoft SQL Server параметры** выберите **"Изменить** поддержку сети" и нажмите кнопку **"Продолжить".**</span><span class="sxs-lookup"><span data-stu-id="52681-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="52681-119">Убедитесь, что для **TCP/IP-сосетей** выбраны все и нажмите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="52681-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="52681-120">Нажмите **кнопку** "Продолжить", чтобы завершить настройку, и завершите настройку.</span><span class="sxs-lookup"><span data-stu-id="52681-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="52681-121">**В Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="52681-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="52681-122">В меню **"Пуск"** выберите **пункты**"Программы", **"Microsoft SQL Server 7.0"** и "Сетевая программа **сервера".**</span><span class="sxs-lookup"><span data-stu-id="52681-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="52681-123">На **вкладке "Общие"** диалоговое окно нажмите кнопку **"Добавить".**</span><span class="sxs-lookup"><span data-stu-id="52681-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="52681-124">В **диалоговом окне** "Добавление конфигурации сетевой библиотеки" щелкните **TCP/IP.**</span><span class="sxs-lookup"><span data-stu-id="52681-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="52681-125">В **полях "Номер порта"** и **"Адрес** прокси-сервера" введите номер порта и прокси-адрес, предоставленные администратором сети.</span><span class="sxs-lookup"><span data-stu-id="52681-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="52681-126">Нажмите **кнопку** "ОК", чтобы завершить настройку, и выйдите из нее.</span><span class="sxs-lookup"><span data-stu-id="52681-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="52681-127">Настройка веб-сервера для использования TCP/IP-sockets</span><span class="sxs-lookup"><span data-stu-id="52681-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="52681-128">Существует два варианта настройки веб-сервера на использование TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="52681-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="52681-129">То, что вы делаете, зависит от того SQL ли все серверы SQL с веб-сервера или только определенный SQL Server доступ с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="52681-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="52681-130">Если все SQL серверы доступны с веб-сервера, необходимо запустить SQL Server клиентской конфигурации на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="52681-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="52681-131">Следующие действия изменяют сетевую библиотеку по умолчанию для всех подключений SQL Server, сделанных с этого веб-сервера IIS, на использование сетевой библиотеки TCP/IP Sockets.</span><span class="sxs-lookup"><span data-stu-id="52681-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="52681-132">**Настройка веб-сервера (всех SQL серверов)**</span><span class="sxs-lookup"><span data-stu-id="52681-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="52681-133">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="52681-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="52681-134">В меню **"Пуск"** найдите пункт "Программы", выберите Microsoft SQL Server **6.5,** а затем выберите SQL **client Configuration Utility.** </span><span class="sxs-lookup"><span data-stu-id="52681-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="52681-135">Перейдите **на вкладку "Net Library".**</span><span class="sxs-lookup"><span data-stu-id="52681-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="52681-136">В поле **"Сеть по** умолчанию" выберите **TCP/IP-sockets.**</span><span class="sxs-lookup"><span data-stu-id="52681-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="52681-137">Нажмите **кнопку "Готово",** чтобы сохранить изменения и выйти из нее.</span><span class="sxs-lookup"><span data-stu-id="52681-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="52681-138">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="52681-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="52681-139">В меню **"Пуск"** выберите **пункты**"Программы", **"Microsoft SQL Server 7.0"** и "Совая программа **клиента".**</span><span class="sxs-lookup"><span data-stu-id="52681-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="52681-140">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="52681-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="52681-141">В поле **сетевой библиотеки по умолчанию** щелкните **TCP/IP.**</span><span class="sxs-lookup"><span data-stu-id="52681-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="52681-142">Нажмите **кнопку "ОК",** чтобы сохранить изменения и выйти из нее.</span><span class="sxs-lookup"><span data-stu-id="52681-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="52681-143">Если определенный SQL Server с веб-сервера, необходимо запустить SQL Server клиентской конфигурации на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="52681-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="52681-144">Чтобы изменить сетевую библиотеку для определенного SQL Server подключения, настройте программное обеспечение клиента SQL Server на компьютере веб-сервера следующим образом.</span><span class="sxs-lookup"><span data-stu-id="52681-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="52681-145">**Настройка веб-сервера (определенного SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="52681-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="52681-146">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="52681-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="52681-147">В меню **"Пуск"** найдите пункт "Программы", выберите Microsoft SQL Server **6.5,** а затем выберите SQL **client Configuration Utility.** </span><span class="sxs-lookup"><span data-stu-id="52681-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="52681-148">Откройте вкладку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="52681-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="52681-149">В поле **"Сервер"** введите имя сервера для подключения с помощью **TCP/IP-sockets.**</span><span class="sxs-lookup"><span data-stu-id="52681-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="52681-150">В поле **"Имя DLL"** выберите **TCP/IP-sockets.**</span><span class="sxs-lookup"><span data-stu-id="52681-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="52681-151">Нажмите **кнопку "Добавить/изменить".**</span><span class="sxs-lookup"><span data-stu-id="52681-151">Click **Add/Modify**.</span></span> <span data-ttu-id="52681-152">Все источники данных, которые указывают на этот сервер, теперь будут использовать TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="52681-152">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="52681-153">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="52681-153">Click **Done**.</span></span>

<span data-ttu-id="52681-154">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="52681-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="52681-155">В меню **"Пуск"** выберите **пункты**"Программы", **"Microsoft SQL Server 7.0"** и "Совластика конфигурации **клиента".**</span><span class="sxs-lookup"><span data-stu-id="52681-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="52681-156">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="52681-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="52681-157">Нажмите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="52681-157">Click **Add**.</span></span>

4.  <span data-ttu-id="52681-158">Введите псевдоним сервера в поле **"Псевдоним сервера".**</span><span class="sxs-lookup"><span data-stu-id="52681-158">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="52681-159">В поле **"Сетевые библиотеки"** щелкните **TCP/IP.**</span><span class="sxs-lookup"><span data-stu-id="52681-159">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="52681-160">В поле **"Имя компьютера"** введите имя компьютера, который прослушивает клиенты TCP/IP Sockets.</span><span class="sxs-lookup"><span data-stu-id="52681-160">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="52681-161">В поле **"Номер порта"** введите порт, по которому SQL Server прослушивает.</span><span class="sxs-lookup"><span data-stu-id="52681-161">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="52681-162">Нажмите **кнопку**"ОК", а затем снова ОК, чтобы выйти из этой сущности. </span><span class="sxs-lookup"><span data-stu-id="52681-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

