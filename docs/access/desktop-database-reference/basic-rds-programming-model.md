---
title: Базовая модель программирования RDS
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 947a6355d07ba2e9fb9b2a9b76c4c1941d83e668
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296887"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="c7384-102">Базовая модель программирования RDS</span><span class="sxs-lookup"><span data-stu-id="c7384-102">Basic RDS programming model</span></span>

<span data-ttu-id="c7384-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7384-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7384-104">RDS направляет приложения, которые существуют в следующей среде: в клиентском приложении указывается программа, которая будет выполняться на сервере, и параметры, необходимые для возврата необходимой информации.</span><span class="sxs-lookup"><span data-stu-id="c7384-104">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information.</span></span> <span data-ttu-id="c7384-105">Программа, вызываемая на сервере, получает доступ к указанному источнику данных, получает сведения, при необходимости обрабатывает данные, а затем возвращает полученные сведения в клиентское приложение в форме, которую можно легко использовать.</span><span class="sxs-lookup"><span data-stu-id="c7384-105">The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use.</span></span> <span data-ttu-id="c7384-106">RDS предоставляет средства для выполнения следующей последовательности действий:</span><span class="sxs-lookup"><span data-stu-id="c7384-106">RDS provides the means for you to perform the following sequence of actions:</span></span>

- <span data-ttu-id="c7384-107">Укажите программу, которая будет вызываться на сервере, и получите способ ссылки на нее из клиента.</span><span class="sxs-lookup"><span data-stu-id="c7384-107">Specify the program to be invoked on the server, and obtain a way to refer to it from the client.</span></span> <span data-ttu-id="c7384-108">(Эта ссылка иногда называется *прокси-сервером*.</span><span class="sxs-lookup"><span data-stu-id="c7384-108">(This reference is sometimes called a *proxy*.</span></span> <span data-ttu-id="c7384-109">Он представляет программу удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="c7384-109">It represents the remote server program.</span></span> <span data-ttu-id="c7384-110">Клиентское приложение выполнит вызов прокси-сервера как локальной программы, но на самом деле вызывает программный удаленный сервер.)</span><span class="sxs-lookup"><span data-stu-id="c7384-110">The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

- <span data-ttu-id="c7384-111">Вызов серверной программы.</span><span class="sxs-lookup"><span data-stu-id="c7384-111">Invoke the server program.</span></span> <span data-ttu-id="c7384-112">Передача параметров в серверную программу, определяющую источник данных, и команды для выпуска.</span><span class="sxs-lookup"><span data-stu-id="c7384-112">Pass parameters to the server program that identify the data source and the command to issue.</span></span> <span data-ttu-id="c7384-113">(Для получения доступа к источнику данных в программе используется ADO.</span><span class="sxs-lookup"><span data-stu-id="c7384-113">(The server program actually uses ADO to gain access to the data source.</span></span> <span data-ttu-id="c7384-114">ADO устанавливает соединение с одним из заданных параметров, а затем выдает команду, указанную в параметре other.</span><span class="sxs-lookup"><span data-stu-id="c7384-114">ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

- <span data-ttu-id="c7384-115">Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных.</span><span class="sxs-lookup"><span data-stu-id="c7384-115">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source.</span></span> <span data-ttu-id="c7384-116">При необходимости объект **Recordset** обрабатывается на сервере.</span><span class="sxs-lookup"><span data-stu-id="c7384-116">Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="c7384-117">Серверная программа возвращает конечный объект **Recordset** клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="c7384-117">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="c7384-118">В клиенте объект **Recordset** помещается в форму, которая может быть легко использоваться визуальными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="c7384-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="c7384-119">Любые изменения объекта **Recordset** отправляются обратно в серверную программу, которая использует их для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="c7384-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="c7384-120">Эта модель программирования содержит некоторые удобные функции.</span><span class="sxs-lookup"><span data-stu-id="c7384-120">This programming model contains certain convenience features.</span></span> <span data-ttu-id="c7384-121">Если для доступа к источнику данных не требуется сложная серверная программа, и если вы указали необходимые параметры подключения и команды, RDS автоматически получите указанные данные с помощью простой серверной программы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7384-121">If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="c7384-122">Если вам нужна более сложная обработка, вы можете указать собственную пользовательскую серверную программу.</span><span class="sxs-lookup"><span data-stu-id="c7384-122">If you need more complex processing, you can specify your own custom server program.</span></span> <span data-ttu-id="c7384-123">Например, так как настраиваемая серверная программа полностью работает с ADO, она может подключаться к нескольким различным источникам данных, объединять данные в сложном способе, а затем возвращать простой, обработанный результат в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="c7384-123">For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="c7384-124">Наконец, если нужны другие задачи, ADO теперь поддерживает настройку поведения программы сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7384-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

