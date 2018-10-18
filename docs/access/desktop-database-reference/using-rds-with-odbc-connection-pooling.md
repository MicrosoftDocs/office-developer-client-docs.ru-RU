---
title: Using RDS with ODBC Connection Pooling
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee66e68cb8eeaaca57c007dc64a9e2b3a8476ec7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606019"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="4c9eb-102">Using RDS with ODBC Connection Pooling</span><span class="sxs-lookup"><span data-stu-id="4c9eb-102">Using RDS with ODBC Connection Pooling</span></span>


<span data-ttu-id="4c9eb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c9eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c9eb-104">Если вы используете источник данных ODBC, можно использовать подключения, группировки в Internet Information Services (IIS) для достижения высокой производительности при обработке нагрузки клиента.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-104">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</span></span> <span data-ttu-id="4c9eb-105">Группировка подключений является руководителем ресурсов для подключений, обслуживание open состояния на часто используемые подключения.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-105">Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="4c9eb-106">Чтобы включить пул подключений, обратитесь к документации служб IIS.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="4c9eb-107"><<<<<<< HEAD примите во внимание, что включение пул подключений может риск веб-сервере другие ограничения, как было указано в документации службы IIS.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-107"><<<<<<< HEAD Please note that enabling connection pooling may subject the Web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
<span data-ttu-id="4c9eb-108">=== Обратите внимание, что включение пул подключений может риск веб-сервере другие ограничения, как было указано в документации службы IIS.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-108">======= Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>
>>>>>>> <span data-ttu-id="4c9eb-109">master</span><span class="sxs-lookup"><span data-stu-id="4c9eb-109">master</span></span>

<span data-ttu-id="4c9eb-110">Чтобы убедиться, что пул подключений стабильным и обеспечивает дополнительную производительность, необходимо настроить Microsoft SQL Server для использования сетевой библиотеки помощью протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-110">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="4c9eb-111">Для этого необходимо:</span><span class="sxs-lookup"><span data-stu-id="4c9eb-111">To do this, you need to:</span></span>

  - <span data-ttu-id="4c9eb-112">Настройка компьютера с SQL Server для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-112">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

<span data-ttu-id="4c9eb-113"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="4c9eb-113"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="4c9eb-114">Настройка веб-сервера для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-114">Configure the Web server to use TCP/IP Sockets.</span></span>
=======
  - <span data-ttu-id="4c9eb-115">Настройка веб-сервера для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-115">Configure the web server to use TCP/IP Sockets.</span></span>
>>>>>>> <span data-ttu-id="4c9eb-116">master</span><span class="sxs-lookup"><span data-stu-id="4c9eb-116">master</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="4c9eb-117">Настройка компьютера SQL Server для использования протокола TCP/IP</span><span class="sxs-lookup"><span data-stu-id="4c9eb-117">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="4c9eb-118">На компьютере с SQL Server запустите программу установки SQL Server, чтобы взаимодействия с источником данных используйте сетевой библиотеки помощью протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-118">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="4c9eb-119">**Чтобы указать сетевой библиотеки помощью протокола TCP/IP на компьютере с SQL Server**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-119">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="4c9eb-120">**В Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-120">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="4c9eb-121">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 6.5**и нажмите кнопку **Установки SQL**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-121">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="4c9eb-122">Дважды нажмите кнопку **Продолжить** .</span><span class="sxs-lookup"><span data-stu-id="4c9eb-122">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="4c9eb-123">В **Microsoft SQL Server — параметры** диалогового окна выберите **Поддержка сети изменения**и нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-123">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="4c9eb-124">Убедитесь, что установлен флажок **Протокола TCP/IP** и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-124">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="4c9eb-125">Нажмите кнопку **Продолжить** для завершения и выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-125">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="4c9eb-126">**В Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-126">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="4c9eb-127">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 7.0**и нажмите кнопку **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-127">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="4c9eb-128">На вкладке **Общие** диалогового окна нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-128">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="4c9eb-129">В диалоговом окне **Добавление конфигурации сетевой библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-129">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="4c9eb-130">В полях **адрес прокси-сервера** и **номер порта** введите предоставляются администратором сети адрес прокси-сервера и номер порта.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-130">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="4c9eb-131">Нажмите **кнопку ОК** , чтобы завершить и выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-131">Click **OK** to finish, and exit setup.</span></span>

<span data-ttu-id="4c9eb-132"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="4c9eb-132"><<<<<<< HEAD</span></span>
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="4c9eb-133">Настройка веб-сервера для использования протокола TCP/IP</span><span class="sxs-lookup"><span data-stu-id="4c9eb-133">Configuring the Web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="4c9eb-134">Существует два варианта для настройки веб-сервера для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-134">There are two options for configuring the Web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="4c9eb-135">Что делать зависит от того, является ли все серверы SQL доступны с сервера на веб-сервер или получить доступ к определенным SQL Server с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-135">What you do depends on whether all SQL Servers are accessed from the Web server, or only a specific SQL Server is accessed from the Web server.</span></span>

<span data-ttu-id="4c9eb-136">Если все серверы SQL доступны с сервера на веб-сервере, необходимо запустить SQL Server служебную программу настройки на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-136">If all SQL Servers are accessed from the Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</span></span> <span data-ttu-id="4c9eb-137">Следующие шаги изменение сетевой библиотеки по умолчанию для всех подключений SQL Server, созданную в этом веб-сервере IIS для использования протокола TCP/IP сетевой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-137">The following steps change the default network library for all SQL Server connections made from this IIS Web server to use the TCP/IP Sockets network library.</span></span>

<a name="to-configure-the-web-server-all-sql-servers"></a><span data-ttu-id="4c9eb-138">**Настройка веб-сервера (все серверы SQL)**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-138">**To configure the Web server (all SQL Servers)**</span></span>
=======
## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="4c9eb-139">Настройка web Server для использования протокола TCP/IP</span><span class="sxs-lookup"><span data-stu-id="4c9eb-139">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="4c9eb-140">Существует два варианта для настройки веб-сервера для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-140">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="4c9eb-141">Что делать зависит от того, является ли все серверы SQL доступны с сервера на веб-сервер или получить доступ к определенным SQL Server с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-141">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="4c9eb-142">Если все серверы SQL доступны с сервера на веб-сервере, необходимо запустить SQL Server служебную программу настройки на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-142">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="4c9eb-143">Следующие шаги изменение сетевой библиотеки по умолчанию для всех подключений SQL Server, созданную в этом веб-сервере IIS для использования протокола TCP/IP сетевой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-143">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="4c9eb-144">**Настройка веб-сервера (все серверы SQL)**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-144">**To configure the web server (all SQL Servers)**</span></span>
>>>>>>> <span data-ttu-id="4c9eb-145">master</span><span class="sxs-lookup"><span data-stu-id="4c9eb-145">master</span></span>

<span data-ttu-id="4c9eb-146">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="4c9eb-147">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 6.5**и нажмите кнопку **Программа настройки клиента SQL**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="4c9eb-148">Перейдите на вкладку **Сетевая библиотека** .</span><span class="sxs-lookup"><span data-stu-id="4c9eb-148">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="4c9eb-149">В поле **Значение по умолчанию сети** выберите **Протокола TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-149">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="4c9eb-150">Нажмите кнопку **Готово** , чтобы сохранить изменения и выйдите из программы.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-150">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="4c9eb-151">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-151">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="4c9eb-152">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 7.0**и нажмите кнопку **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-152">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="4c9eb-153">Перейдите на вкладку **Общие** .</span><span class="sxs-lookup"><span data-stu-id="4c9eb-153">Click the **General** tab.</span></span>

3.  <span data-ttu-id="4c9eb-154">В поле **по умолчанию сетевой библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-154">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="4c9eb-155">Нажмите **кнопку ОК** , чтобы сохранить изменения и выйдите из программы.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-155">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="4c9eb-156"><<<<<<< HEAD определенного сервера SQL Server доступен на веб-сервере, требуется ли запуск служебной программы настройки SQL Server клиента на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-156"><<<<<<< HEAD If a specific SQL Server is accessed from a Web server, you need to run the SQL Server Client Configuration Utility on the Web server computer.</span></span> <span data-ttu-id="4c9eb-157">Чтобы изменить сетевой библиотеки для конкретного подключения к SQL Server, настройте программное обеспечение клиента SQL Server на компьютере веб-сервера следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-157">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the Web server computer as follows.</span></span>

<a name="to-configure-the-web-server-a-specific-sql-server"></a><span data-ttu-id="4c9eb-158">**Настройка веб-сервера (определенного сервера SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-158">**To configure the Web server (a specific SQL Server)**</span></span>
=======
<span data-ttu-id="4c9eb-159">При обращении к ним определенного сервера SQL Server с веб-сервера, необходимо запустить SQL Server служебную программу настройки на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-159">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="4c9eb-160">Чтобы изменить сетевой библиотеки для конкретного подключения к SQL Server, настройте программное обеспечение клиента SQL Server на компьютере веб-сервера следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-160">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="4c9eb-161">**Настройка веб-сервера (определенного сервера SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-161">**To configure the web server (a specific SQL Server)**</span></span>
>>>>>>> <span data-ttu-id="4c9eb-162">master</span><span class="sxs-lookup"><span data-stu-id="4c9eb-162">master</span></span>

<span data-ttu-id="4c9eb-163">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-163">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="4c9eb-164">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 6.5**и нажмите кнопку **Программа настройки клиента SQL**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-164">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="4c9eb-165">Перейдите на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="4c9eb-165">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="4c9eb-166">В поле **сервер** введите имя сервера для подключения с помощью **Протокола TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-166">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="4c9eb-167">В поле **Имя библиотеки DLL** установите **Протокола TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-167">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="4c9eb-168">Нажмите кнопку **Добавить/изменить**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-168">Click **Add/Modify**.</span></span> <span data-ttu-id="4c9eb-169">Теперь все источники данных, указывающая на этот сервер будет использоваться протокол TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-169">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="4c9eb-170">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-170">Click **Done**.</span></span>

<span data-ttu-id="4c9eb-171">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="4c9eb-171">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="4c9eb-172">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 7.0**и нажмите кнопку **Программа настройки клиента**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-172">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="4c9eb-173">Перейдите на вкладку **Общие** .</span><span class="sxs-lookup"><span data-stu-id="4c9eb-173">Click the **General** tab.</span></span>

3.  <span data-ttu-id="4c9eb-174">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-174">Click **Add**.</span></span>

4.  <span data-ttu-id="4c9eb-175">В поле **псевдоним сервера** введите псевдоним сервера.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-175">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="4c9eb-176">В поле **сетевые библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-176">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="4c9eb-177">В поле **имя компьютера** введите имя компьютера, который прослушивает клиентов соединителей TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-177">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="4c9eb-178">В поле **номер порта** введите номер порта, который прослушивает SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-178">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="4c9eb-179">Нажмите **кнопку ОК**, а затем **кнопку ОК** еще раз, чтобы выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="4c9eb-179">Click **OK**, and then **OK** again to exit the utility.</span></span>

