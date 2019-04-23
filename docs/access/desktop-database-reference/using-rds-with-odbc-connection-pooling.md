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
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="6f77f-102">Использование RDS с группировкой подключений ODBC</span><span class="sxs-lookup"><span data-stu-id="6f77f-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="6f77f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f77f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f77f-104">Если вы используете источник данных ODBC, вы можете использовать параметр пулов подключений в службах IIS для обеспечения высокой производительности нагрузки клиентов.</span><span class="sxs-lookup"><span data-stu-id="6f77f-104">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</span></span> <span data-ttu-id="6f77f-105">Пул подключений является диспетчером ресурсов для подключений, сохраняя открытое состояние в часто используемых подключениях.</span><span class="sxs-lookup"><span data-stu-id="6f77f-105">Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="6f77f-106">Для включения пула подключений обратитесь к документации Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="6f77f-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="6f77f-107">Обратите внимание, что включение пула подключений может привести к перечислению веб-сервера на другие ограничения, как указано в документации Microsoft Internet Information Services.</span><span class="sxs-lookup"><span data-stu-id="6f77f-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="6f77f-108">Чтобы обеспечить стабильность пула подключений и повышения производительности, необходимо настроить Microsoft SQL Server для использования сетевой библиотеки сокетов TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6f77f-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="6f77f-109">Для этого необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6f77f-109">To do this, you need to:</span></span>

  - <span data-ttu-id="6f77f-110">Настройка компьютера с SQL Server для использования сокетов TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6f77f-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="6f77f-111">Настройте веб-сервер для использования сокетов TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6f77f-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="6f77f-112">Настройка компьютера с SQL Server для использования сокетов TCP/IP</span><span class="sxs-lookup"><span data-stu-id="6f77f-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="6f77f-113">На компьютере с SQL Server запустите программу установки SQL Server, чтобы при взаимодействии с источником данных использовалась сетевая библиотека сокетов TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6f77f-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="6f77f-114">**Указание сетевой библиотеки сокетов TCP/IP на компьютере с SQL Server**</span><span class="sxs-lookup"><span data-stu-id="6f77f-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="6f77f-115">**В Microsoft SQL Server 6,5:**</span><span class="sxs-lookup"><span data-stu-id="6f77f-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="6f77f-116">В меню **Пуск** выберите **программы**, затем **Microsoft SQL Server 6,5**и щелкните **Установка SQL**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="6f77f-117">Дважды нажмите кнопку **продолжить** .</span><span class="sxs-lookup"><span data-stu-id="6f77f-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="6f77f-118">В диалоговом окне **Параметры Microsoft SQL Server** выберите **Изменить сетевую поддержку**, а затем нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="6f77f-119">Убедитесь, что установлен флажок **сокеты TCP/IP** , и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="6f77f-120">Нажмите кнопку **Далее** , чтобы завершить работу и выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="6f77f-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="6f77f-121">**В Microsoft SQL Server 7,0:**</span><span class="sxs-lookup"><span data-stu-id="6f77f-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="6f77f-122">В меню **Пуск** последовательно выберите пункты **программы**, **Microsoft SQL Server 7,0**и **сетевое средство сервера**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="6f77f-123">На вкладке " **Общие** " диалогового окна нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="6f77f-124">В диалоговом окне **Добавление конфигурации сетевой библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="6f77f-125">В поля **номер порта** и **адрес прокси-сервера** введите номер порта и адрес прокси-сервера, предоставленные администратором сети.</span><span class="sxs-lookup"><span data-stu-id="6f77f-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="6f77f-126">Нажмите кнопку **ОК** , чтобы завершить работу, и закройте программу установки.</span><span class="sxs-lookup"><span data-stu-id="6f77f-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="6f77f-127">Настройка веб-сервера для использования сокетов TCP/IP</span><span class="sxs-lookup"><span data-stu-id="6f77f-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="6f77f-128">Настроить веб-сервер для использования сокетов TCP/IP можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="6f77f-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="6f77f-129">Действия, которые вы выполняете, зависят от того, доступны ли все серверы SQL с веб-сервера, или доступ к конкретному серверу SQL с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="6f77f-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="6f77f-130">Если доступ ко всем серверам SQL Server осуществляется с веб-сервера, необходимо запустить служебную программу настройки клиента SQL Server на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="6f77f-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="6f77f-131">Следующие действия изменяют сетевую библиотеку по умолчанию для всех подключений SQL Server, выполняемых с этого веб-сервера IIS, для использования сетевой библиотеки TCP/IP Sockets.</span><span class="sxs-lookup"><span data-stu-id="6f77f-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="6f77f-132">**Настройка веб-сервера (все серверы SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="6f77f-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="6f77f-133">**Для Microsoft SQL Server 6,5:**</span><span class="sxs-lookup"><span data-stu-id="6f77f-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="6f77f-134">В меню **Пуск** выберите **программы**, затем **Microsoft SQL Server 6,5**и щелкните **служебная программа настройки клиента SQL**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="6f77f-135">Перейдите на вкладку **Библиотека NET** .</span><span class="sxs-lookup"><span data-stu-id="6f77f-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="6f77f-136">В поле **сеть по умолчанию** выберите **сокеты TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="6f77f-137">Нажмите кнопку **Готово** , чтобы сохранить изменения и выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="6f77f-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="6f77f-138">**Для Microsoft SQL Server 7,0:**</span><span class="sxs-lookup"><span data-stu-id="6f77f-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="6f77f-139">В меню **Пуск** последовательно выберите пункты **программы**, **Microsoft SQL Server 7,0**и **служебная сеть клиента**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="6f77f-140">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="6f77f-141">В поле **Сетевая библиотека по умолчанию** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="6f77f-142">Нажмите кнопку **ОК** , чтобы сохранить изменения и выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="6f77f-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="6f77f-143">Если доступ к определенному серверу SQL Server осуществляется с веб-сервера, необходимо запустить служебную программу настройки клиента SQL Server на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="6f77f-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="6f77f-144">Чтобы изменить сетевую библиотеку для конкретного подключения к SQL Server, настройте клиентское программное обеспечение SQL Server на компьютере веб-сервера следующим образом.</span><span class="sxs-lookup"><span data-stu-id="6f77f-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="6f77f-145">**Настройка веб-сервера (определенного сервера SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="6f77f-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="6f77f-146">**Для Microsoft SQL Server 6,5:**</span><span class="sxs-lookup"><span data-stu-id="6f77f-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="6f77f-147">В меню **Пуск** выберите **программы**, затем **Microsoft SQL Server 6,5**и щелкните **служебная программа настройки клиента SQL**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="6f77f-148">Откройте вкладку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="6f77f-149">В поле **сервер** введите имя сервера, к которому необходимо подключиться с помощью сокетов **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="6f77f-150">В поле **имя библиотеки DLL** выберите пункт **сокеты TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="6f77f-151">Нажмите кнопку **Добавить/изменить**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-151">Click **Add/Modify**.</span></span> <span data-ttu-id="6f77f-152">Все источники данных, указывающие на этот сервер, теперь будут использовать сокеты TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6f77f-152">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="6f77f-153">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-153">Click **Done**.</span></span>

<span data-ttu-id="6f77f-154">**Для Microsoft SQL Server 7,0:**</span><span class="sxs-lookup"><span data-stu-id="6f77f-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="6f77f-155">В меню **Пуск** последовательно выберите пункты **программы**, **Microsoft SQL Server 7,0**и **служебная программа настройки клиента**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="6f77f-156">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="6f77f-157">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-157">Click **Add**.</span></span>

4.  <span data-ttu-id="6f77f-158">Введите псевдоним сервера в поле **псевдоним сервера** .</span><span class="sxs-lookup"><span data-stu-id="6f77f-158">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="6f77f-159">В поле **сетевые библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="6f77f-159">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="6f77f-160">В поле **имя компьютера** введите имя компьютера, который прослушивает клиентов сокетов TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6f77f-160">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="6f77f-161">В поле **номер порта введите номер** порта, на котором проСлушивается SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6f77f-161">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="6f77f-162">Нажмите кнопку **ОК**, а затем снова кнопку **ОК** , чтобы выйти из служебной программы.</span><span class="sxs-lookup"><span data-stu-id="6f77f-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

