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
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="70e68-102">Использование RDS с группировкой подключений ODBC</span><span class="sxs-lookup"><span data-stu-id="70e68-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="70e68-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70e68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70e68-104">Если вы используете источник данных ODBC, вы можете использовать параметр пулинга подключения в службы IIS (IIS) для обеспечения высокой производительности обработки клиентской нагрузки.</span><span class="sxs-lookup"><span data-stu-id="70e68-104">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</span></span> <span data-ttu-id="70e68-105">Объединение подключений — это диспетчер ресурсов для подключений, который поддерживает открытое состояние для часто используемых подключений.</span><span class="sxs-lookup"><span data-stu-id="70e68-105">Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="70e68-106">Чтобы включить объединение подключений, обратитесь к службы IIS документации.</span><span class="sxs-lookup"><span data-stu-id="70e68-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="70e68-107">Обратите внимание, что включение пула подключений может привести к другим ограничениям на веб-сервер, как отмечено в Microsoft IIS документации.</span><span class="sxs-lookup"><span data-stu-id="70e68-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="70e68-108">Чтобы обеспечить стабильность пула подключений и дополнительные достижения производительности, необходимо настроить Microsoft SQL Server для использования сетевой библиотеки TCP/IP Socket.</span><span class="sxs-lookup"><span data-stu-id="70e68-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="70e68-109">Для этого необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="70e68-109">To do this, you need to:</span></span>

  - <span data-ttu-id="70e68-110">Настройка компьютера SQL Server для использования TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="70e68-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="70e68-111">Настройка веб-сервера для использования TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="70e68-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="70e68-112">Настройка компьютера SQL Server для использования TCP/IP-sockets</span><span class="sxs-lookup"><span data-stu-id="70e68-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="70e68-113">На компьютере SQL Server запустите программу установки SQL Server, чтобы взаимодействия с источником данных использовали библиотеку сети TCP/IP Socket.</span><span class="sxs-lookup"><span data-stu-id="70e68-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="70e68-114">**Указание сетевой библиотеки TCP/IP socket на SQL Server компьютере**</span><span class="sxs-lookup"><span data-stu-id="70e68-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="70e68-115">**В Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="70e68-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="70e68-116">Из меню **Пуск** указать на **программы**, указать на Microsoft SQL Server **6.5**, а затем **нажмите кнопку SQL установки**.</span><span class="sxs-lookup"><span data-stu-id="70e68-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="70e68-117">Нажмите **кнопку Продолжить** дважды.</span><span class="sxs-lookup"><span data-stu-id="70e68-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="70e68-118">В **диалоговом окне Microsoft SQL Server параметры** выберите **службу поддержки** сети изменения и нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="70e68-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="70e68-119">Убедитесь, что **выбрано окно TCP/IP Sockets,** и нажмите **кнопку ОК.**</span><span class="sxs-lookup"><span data-stu-id="70e68-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="70e68-120">Нажмите **кнопку Продолжить,** чтобы закончить, и выйти установки.</span><span class="sxs-lookup"><span data-stu-id="70e68-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="70e68-121">**В Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="70e68-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="70e68-122">Из меню **"Пуск"** указать на **программы**, указать на Microsoft SQL Server **7.0,** а затем нажмите **кнопку Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="70e68-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="70e68-123">На **вкладке General** в диалоговом окне нажмите **кнопку Добавить**.</span><span class="sxs-lookup"><span data-stu-id="70e68-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="70e68-124">В **диалоговом окне** Настройка конфигурации библиотеки добавить сеть щелкните **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="70e68-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="70e68-125">В **полях номер порта** и **адрес прокси** введите номер порта и прокси-адрес, предоставленные администратором сети.</span><span class="sxs-lookup"><span data-stu-id="70e68-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="70e68-126">Нажмите **кнопку ОК,** чтобы завершить и выйти из установки.</span><span class="sxs-lookup"><span data-stu-id="70e68-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="70e68-127">Настройка веб-сервера для использования TCP/IP-розеток</span><span class="sxs-lookup"><span data-stu-id="70e68-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="70e68-128">Существует два варианта настройки веб-сервера для использования TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="70e68-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="70e68-129">То, что вы делаете, зависит от того, SQL серверы доступны с веб-сервера или только определенный SQL Server доступ с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="70e68-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="70e68-130">Если все SQL серверы доступны с веб-сервера, необходимо выполнить SQL Server службу конфигурации клиента на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="70e68-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="70e68-131">В следующих действиях библиотека сети по умолчанию SQL Server всех подключений, сделанных с этого веб-сервера IIS, для использования сетевой библиотеки TCP/IP Sockets.</span><span class="sxs-lookup"><span data-stu-id="70e68-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="70e68-132">**Настройка веб-сервера (все SQL серверы)**</span><span class="sxs-lookup"><span data-stu-id="70e68-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="70e68-133">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="70e68-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="70e68-134">Из меню **Пуск** указать на программы **,** указать на Microsoft SQL Server **6.5**, а затем нажмите кнопку SQL **конфигурации клиента утилиты**.</span><span class="sxs-lookup"><span data-stu-id="70e68-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="70e68-135">Щелкните **вкладку "Чистая библиотека".**</span><span class="sxs-lookup"><span data-stu-id="70e68-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="70e68-136">В поле **Сеть по умолчанию** выберите **TCP/IP-розетки.**</span><span class="sxs-lookup"><span data-stu-id="70e68-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="70e68-137">Нажмите **кнопку Сделано,** чтобы сохранить изменения и выйти из утилиты.</span><span class="sxs-lookup"><span data-stu-id="70e68-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="70e68-138">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="70e68-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="70e68-139">Из меню **Пуск** указать на **программы**, указать на Microsoft SQL Server **7.0,** а затем нажмите **кнопку Клиентская сеть утилита**.</span><span class="sxs-lookup"><span data-stu-id="70e68-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="70e68-140">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="70e68-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="70e68-141">В поле **сетевой библиотеки по умолчанию** щелкните **TCP/IP.**</span><span class="sxs-lookup"><span data-stu-id="70e68-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="70e68-142">Нажмите **кнопку ОК,** чтобы сохранить изменения и выйти из утилиты.</span><span class="sxs-lookup"><span data-stu-id="70e68-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="70e68-143">Если определенный SQL Server с веб-сервера, необходимо выполнить SQL Server службу конфигурации клиента на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="70e68-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="70e68-144">Чтобы изменить библиотеку сети для определенного подключения SQL Server, настройте программное обеспечение SQL Server клиента на компьютере веб-сервера следующим образом.</span><span class="sxs-lookup"><span data-stu-id="70e68-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="70e68-145">**Настройка веб-сервера (определенного SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="70e68-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="70e68-146">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="70e68-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="70e68-147">Из меню **Пуск** указать на программы **,** указать на Microsoft SQL Server **6.5**, а затем нажмите кнопку SQL **конфигурации клиента утилиты**.</span><span class="sxs-lookup"><span data-stu-id="70e68-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="70e68-148">Откройте вкладку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="70e68-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="70e68-149">В поле **Server** введите имя сервера для подключения к использованию **TCP/IP-sockets.**</span><span class="sxs-lookup"><span data-stu-id="70e68-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="70e68-150">В поле **Имя DLL** выберите **TCP/IP-розетки.**</span><span class="sxs-lookup"><span data-stu-id="70e68-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="70e68-151">Нажмите **кнопку Добавить/Изменить**.</span><span class="sxs-lookup"><span data-stu-id="70e68-151">Click **Add/Modify**.</span></span> <span data-ttu-id="70e68-152">Все источники данных, указывающие на этот сервер, теперь будут использовать TCP/IP-sockets.</span><span class="sxs-lookup"><span data-stu-id="70e68-152">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="70e68-153">Нажмите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="70e68-153">Click **Done**.</span></span>

<span data-ttu-id="70e68-154">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="70e68-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="70e68-155">Из меню **Пуск** указать на **программы**, указать на Microsoft SQL Server **7.0,** а затем нажмите **кнопку Конфигурация клиента Утилита**.</span><span class="sxs-lookup"><span data-stu-id="70e68-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="70e68-156">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="70e68-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="70e68-157">Нажмите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="70e68-157">Click **Add**.</span></span>

4.  <span data-ttu-id="70e68-158">Введите псевдоним сервера в поле **псевдонима Server.**</span><span class="sxs-lookup"><span data-stu-id="70e68-158">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="70e68-159">В поле **Сетевые библиотеки** щелкните **TCP/IP.**</span><span class="sxs-lookup"><span data-stu-id="70e68-159">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="70e68-160">В поле **Имя компьютера** введите имя компьютера, прослушиваемого для клиентов TCP/IP Sockets.</span><span class="sxs-lookup"><span data-stu-id="70e68-160">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="70e68-161">В поле **Номер порта** введите порт, в котором SQL Server прослушивает.</span><span class="sxs-lookup"><span data-stu-id="70e68-161">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="70e68-162">Нажмите **кнопку ОК,** а **затем снова ОК,** чтобы выйти из утилиты.</span><span class="sxs-lookup"><span data-stu-id="70e68-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

