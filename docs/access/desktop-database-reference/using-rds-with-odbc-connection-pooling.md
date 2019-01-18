---
title: Использование RDS с группировкой подключений ODBC
TOCTitle: Using RDS with ODBC Connection Pooling
ms:assetid: 6e8b023a-d211-44cb-10af-d43174a5d4bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249437(v=office.15)
ms:contentKeyID: 48545513
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87d380fdc52cdee2aa834fd6e78ff1b761a0e93a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706368"
---
# <a name="using-rds-with-odbc-connection-pooling"></a><span data-ttu-id="49781-102">Использование RDS с группировкой подключений ODBC</span><span class="sxs-lookup"><span data-stu-id="49781-102">Using RDS with ODBC connection pooling</span></span>


<span data-ttu-id="49781-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49781-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49781-104">Если вы используете источник данных ODBC, можно использовать подключения, группировки в Internet Information Services (IIS) для достижения высокой производительности при обработке нагрузки клиента.</span><span class="sxs-lookup"><span data-stu-id="49781-104">If you're using an ODBC data source, you can use the connection pooling option in Internet Information Services (IIS) to achieve high performance handling of client load.</span></span> <span data-ttu-id="49781-105">Группировка подключений является руководителем ресурсов для подключений, обслуживание open состояния на часто используемые подключения.</span><span class="sxs-lookup"><span data-stu-id="49781-105">Connection pooling is a resource manager for connections, maintaining the open state on frequently used connections.</span></span>

<span data-ttu-id="49781-106">Чтобы включить пул подключений, обратитесь к документации служб IIS.</span><span class="sxs-lookup"><span data-stu-id="49781-106">To enable connection pooling, refer to the Internet Information Services documentation.</span></span>

<span data-ttu-id="49781-107">Обратите внимание, что включение пул подключений может риск веб-сервере другие ограничения, как было указано в документации службы IIS.</span><span class="sxs-lookup"><span data-stu-id="49781-107">Please note that enabling connection pooling may subject the web server to other restrictions, as noted in the Microsoft Internet Information Services documentation.</span></span>

<span data-ttu-id="49781-108">Чтобы убедиться, что пул подключений стабильным и обеспечивает дополнительную производительность, необходимо настроить Microsoft SQL Server для использования сетевой библиотеки помощью протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-108">To ensure that connection pooling is stable and provides additional performance gains, you must configure Microsoft SQL Server to use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="49781-109">Для этого необходимо:</span><span class="sxs-lookup"><span data-stu-id="49781-109">To do this, you need to:</span></span>

  - <span data-ttu-id="49781-110">Настройка компьютера с SQL Server для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-110">Configure the SQL Server computer to use TCP/IP Sockets.</span></span>

  - <span data-ttu-id="49781-111">Настройка веб-сервера для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-111">Configure the web server to use TCP/IP Sockets.</span></span>

## <a name="configuring-the-sql-server-computer-to-use-tcpip-sockets"></a><span data-ttu-id="49781-112">Настройка компьютера SQL Server для использования протокола TCP/IP</span><span class="sxs-lookup"><span data-stu-id="49781-112">Configuring the SQL Server Computer to Use TCP/IP Sockets</span></span>

<span data-ttu-id="49781-113">На компьютере с SQL Server запустите программу установки SQL Server, чтобы взаимодействия с источником данных используйте сетевой библиотеки помощью протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-113">On the SQL Server computer, run the SQL Server Setup program so that interactions with the data source use the TCP/IP Socket network library.</span></span>

<span data-ttu-id="49781-114">**Чтобы указать сетевой библиотеки помощью протокола TCP/IP на компьютере с SQL Server**</span><span class="sxs-lookup"><span data-stu-id="49781-114">**To specify the TCP/IP Socket network library on the SQL Server computer**</span></span>

<span data-ttu-id="49781-115">**В Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="49781-115">**In Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="49781-116">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 6.5**и нажмите кнопку **Установки SQL**.</span><span class="sxs-lookup"><span data-stu-id="49781-116">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Setup**.</span></span>

2.  <span data-ttu-id="49781-117">Дважды нажмите кнопку **Продолжить** .</span><span class="sxs-lookup"><span data-stu-id="49781-117">Click **Continue** twice.</span></span>

3.  <span data-ttu-id="49781-118">В **Microsoft SQL Server — параметры** диалогового окна выберите **Поддержка сети изменения**и нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="49781-118">In the **Microsoft SQL Server — Options** dialog box, select **Change Network Support**, and then click **Continue**.</span></span>

4.  <span data-ttu-id="49781-119">Убедитесь, что установлен флажок **Протокола TCP/IP** и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="49781-119">Make sure the **TCP/IP Sockets** check box is selected, and click **OK**.</span></span>

5.  <span data-ttu-id="49781-120">Нажмите кнопку **Продолжить** для завершения и выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="49781-120">Click **Continue** to finish, and exit setup.</span></span>

<span data-ttu-id="49781-121">**В Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="49781-121">**In Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="49781-122">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 7.0**и нажмите кнопку **Server Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="49781-122">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Server Network Utility**.</span></span>

2.  <span data-ttu-id="49781-123">На вкладке **Общие** диалогового окна нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="49781-123">On the **General** tab of the dialog box, click **Add**.</span></span>

3.  <span data-ttu-id="49781-124">В диалоговом окне **Добавление конфигурации сетевой библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="49781-124">In the **Add Network Library Configuration** dialog box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="49781-125">В полях **адрес прокси-сервера** и **номер порта** введите предоставляются администратором сети адрес прокси-сервера и номер порта.</span><span class="sxs-lookup"><span data-stu-id="49781-125">In the **Port number** and **Proxy address** boxes, enter the port number and proxy address provided by your network administrator.</span></span>

5.  <span data-ttu-id="49781-126">Нажмите **кнопку ОК** , чтобы завершить и выйти из программы установки.</span><span class="sxs-lookup"><span data-stu-id="49781-126">Click **OK** to finish, and exit setup.</span></span>

## <a name="configuring-the-web-server-to-use-tcpip-sockets"></a><span data-ttu-id="49781-127">Настройка web Server для использования протокола TCP/IP</span><span class="sxs-lookup"><span data-stu-id="49781-127">Configuring the web Server to Use TCP/IP Sockets</span></span>

<span data-ttu-id="49781-128">Существует два варианта для настройки веб-сервера для использования протокола TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-128">There are two options for configuring the web server to use TCP/IP Sockets.</span></span> <span data-ttu-id="49781-129">Что делать зависит от того, является ли все серверы SQL доступны с сервера на веб-сервер или получить доступ к определенным SQL Server с веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="49781-129">What you do depends on whether all SQL Servers are accessed from the web server, or only a specific SQL Server is accessed from the web server.</span></span>

<span data-ttu-id="49781-130">Если все серверы SQL доступны с сервера на веб-сервере, необходимо запустить SQL Server служебную программу настройки на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="49781-130">If all SQL Servers are accessed from the web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="49781-131">Следующие шаги изменение сетевой библиотеки по умолчанию для всех подключений SQL Server, созданную в этом веб-сервере IIS для использования протокола TCP/IP сетевой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="49781-131">The following steps change the default network library for all SQL Server connections made from this IIS web server to use the TCP/IP Sockets network library.</span></span>

<span data-ttu-id="49781-132">**Настройка веб-сервера (все серверы SQL)**</span><span class="sxs-lookup"><span data-stu-id="49781-132">**To configure the web server (all SQL Servers)**</span></span>

<span data-ttu-id="49781-133">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="49781-133">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="49781-134">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 6.5**и нажмите кнопку **Программа настройки клиента SQL**.</span><span class="sxs-lookup"><span data-stu-id="49781-134">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="49781-135">Перейдите на вкладку **Сетевая библиотека** .</span><span class="sxs-lookup"><span data-stu-id="49781-135">Click the **Net Library** tab.</span></span>

3.  <span data-ttu-id="49781-136">В поле **Значение по умолчанию сети** выберите **Протокола TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="49781-136">In the **Default Network** box, select **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="49781-137">Нажмите кнопку **Готово** , чтобы сохранить изменения и выйдите из программы.</span><span class="sxs-lookup"><span data-stu-id="49781-137">Click **Done** to save changes and exit the utility.</span></span>

<span data-ttu-id="49781-138">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="49781-138">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="49781-139">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 7.0**и нажмите кнопку **Client Network Utility**.</span><span class="sxs-lookup"><span data-stu-id="49781-139">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Network Utility**.</span></span>

2.  <span data-ttu-id="49781-140">Перейдите на вкладку **Общие** .</span><span class="sxs-lookup"><span data-stu-id="49781-140">Click the **General** tab.</span></span>

3.  <span data-ttu-id="49781-141">В поле **по умолчанию сетевой библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="49781-141">In the **Default network library** box, click **TCP/IP**.</span></span>

4.  <span data-ttu-id="49781-142">Нажмите **кнопку ОК** , чтобы сохранить изменения и выйдите из программы.</span><span class="sxs-lookup"><span data-stu-id="49781-142">Click **OK** to save changes and exit the utility.</span></span>

<span data-ttu-id="49781-143">При обращении к ним определенного сервера SQL Server с веб-сервера, необходимо запустить SQL Server служебную программу настройки на компьютере веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="49781-143">If a specific SQL Server is accessed from a web server, you need to run the SQL Server Client Configuration Utility on the web server computer.</span></span> <span data-ttu-id="49781-144">Чтобы изменить сетевой библиотеки для конкретного подключения к SQL Server, настройте программное обеспечение клиента SQL Server на компьютере веб-сервера следующим образом.</span><span class="sxs-lookup"><span data-stu-id="49781-144">To change the network library for a specific SQL Server connection, configure the SQL Server Client software on the web server computer as follows.</span></span>

<span data-ttu-id="49781-145">**Настройка веб-сервера (определенного сервера SQL Server)**</span><span class="sxs-lookup"><span data-stu-id="49781-145">**To configure the web server (a specific SQL Server)**</span></span>

<span data-ttu-id="49781-146">**Для Microsoft SQL Server 6.5:**</span><span class="sxs-lookup"><span data-stu-id="49781-146">**For Microsoft SQL Server 6.5:**</span></span>

1.  <span data-ttu-id="49781-147">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 6.5**и нажмите кнопку **Программа настройки клиента SQL**.</span><span class="sxs-lookup"><span data-stu-id="49781-147">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 6.5**, and then click **SQL Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="49781-148">Перейдите на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="49781-148">Click the **Advanced** tab.</span></span>

3.  <span data-ttu-id="49781-149">В поле **сервер** введите имя сервера для подключения с помощью **Протокола TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="49781-149">In the **Server** box, type the name of the server to connect to using **TCP/IP Sockets**.</span></span>

4.  <span data-ttu-id="49781-150">В поле **Имя библиотеки DLL** установите **Протокола TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="49781-150">In the **DLL Name** box, select **TCP/IP Sockets**.</span></span>

5.  <span data-ttu-id="49781-151">Нажмите кнопку **Добавить/изменить**.</span><span class="sxs-lookup"><span data-stu-id="49781-151">Click **Add/Modify**.</span></span> <span data-ttu-id="49781-152">Теперь все источники данных, указывающая на этот сервер будет использоваться протокол TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-152">All data sources pointing to this server will now use TCP/IP Sockets.</span></span>

6.  <span data-ttu-id="49781-153">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="49781-153">Click **Done**.</span></span>

<span data-ttu-id="49781-154">**Для Microsoft SQL Server 7.0:**</span><span class="sxs-lookup"><span data-stu-id="49781-154">**For Microsoft SQL Server 7.0:**</span></span>

1.  <span data-ttu-id="49781-155">Из меню **Пуск** выберите **программы**, выберите пункт **Microsoft SQL Server 7.0**и нажмите кнопку **Программа настройки клиента**.</span><span class="sxs-lookup"><span data-stu-id="49781-155">From the **Start** menu, point to **Programs**, point to **Microsoft SQL Server 7.0**, and then click **Client Configuration Utility**.</span></span>

2.  <span data-ttu-id="49781-156">Перейдите на вкладку **Общие** .</span><span class="sxs-lookup"><span data-stu-id="49781-156">Click the **General** tab.</span></span>

3.  <span data-ttu-id="49781-157">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="49781-157">Click **Add**.</span></span>

4.  <span data-ttu-id="49781-158">В поле **псевдоним сервера** введите псевдоним сервера.</span><span class="sxs-lookup"><span data-stu-id="49781-158">Enter the alias of the server in the **Server alias** box.</span></span> <span data-ttu-id="49781-159">В поле **сетевые библиотеки** выберите **TCP/IP**.</span><span class="sxs-lookup"><span data-stu-id="49781-159">In the **Network libraries** box, click **TCP/IP**.</span></span> <span data-ttu-id="49781-160">В поле **имя компьютера** введите имя компьютера, который прослушивает клиентов соединителей TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49781-160">In the **Computer name** box, enter the computer name of the computer that listens for TCP/IP Sockets clients.</span></span> <span data-ttu-id="49781-161">В поле **номер порта** введите номер порта, который прослушивает SQL Server.</span><span class="sxs-lookup"><span data-stu-id="49781-161">In the **Port number** box, enter the port on which the SQL Server listens.</span></span>

5.  <span data-ttu-id="49781-162">Нажмите **кнопку ОК**, а затем **кнопку ОК** еще раз, чтобы выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="49781-162">Click **OK**, and then **OK** again to exit the utility.</span></span>

