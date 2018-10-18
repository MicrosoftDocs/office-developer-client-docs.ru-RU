---
title: Solutions for Remote Data Access
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45164401bbab5cc9134fa7a354fde54bbb02fa37
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604787"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="7fcd7-102">Solutions for Remote Data Access</span><span class="sxs-lookup"><span data-stu-id="7fcd7-102">Solutions for Remote Data Access</span></span>


<span data-ttu-id="7fcd7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fcd7-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="7fcd7-104">Проблемы</span><span class="sxs-lookup"><span data-stu-id="7fcd7-104">The Issue</span></span>

<span data-ttu-id="7fcd7-105">ADO позволяет приложению непосредственно получить доступ к и изменять источники данных (иногда называемую двухуровневой системы).</span><span class="sxs-lookup"><span data-stu-id="7fcd7-105">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system).</span></span> <span data-ttu-id="7fcd7-106">Например при подключении к источнику данных, который содержит данные, являющегося прямое подключение в двухуровневой системы.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-106">For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="7fcd7-107">Тем не менее можно получить доступ к источникам данных косвенно через промежуточное таких как Microsoft® Internet сведения Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="7fcd7-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft® Internet Information Services (IIS).</span></span> <span data-ttu-id="7fcd7-108">Упорядочение иногда называется трехуровневой системы.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="7fcd7-109">Службы IIS — это система клиента и сервера, который позволяет эффективно для локальной или клиента, приложения для запуска программы удаленного или сервера, через Интернет или интрасети.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="7fcd7-110">Программа сервер получает доступ к источнику данных и при необходимости обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="7fcd7-111"><<<<<<< Пример HEAD для веб-страницы интрасети содержит приложение, записанные в Microsoft® Visual Basic Scripting Edition (VBScript), который подключается к IIS.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-111"><<<<<<< HEAD For example, your intranet Web page contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="7fcd7-112">Службы IIS по очереди подключается к источнику данных, получает данные, обрабатывает каким-либо образом и затем возвращает обработанные сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>
<span data-ttu-id="7fcd7-113">===, Например веб-страница интрасети содержит приложения в Microsoft® Visual Basic Scripting Edition (VBScript), который подключается к IIS.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-113">======= For example, your intranet webpage contains an application written in Microsoft® Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="7fcd7-114">Службы IIS по очереди подключается к источнику данных, получает данные, обрабатывает каким-либо образом и затем возвращает обработанные сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-114">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>
>>>>>>> <span data-ttu-id="7fcd7-115">master</span><span class="sxs-lookup"><span data-stu-id="7fcd7-115">master</span></span>

<span data-ttu-id="7fcd7-116">В этом примере приложения никогда не непосредственно подключенные к источнику данных; Были служб IIS.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-116">In this example, your application never directly connected to the data source; IIS did.</span></span> <span data-ttu-id="7fcd7-117">И IIS получить доступ к данным с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-117">And IIS accessed the data by means of ADO.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7fcd7-118">Клиента и сервера приложений не имеет на основе в Интернете или интрасети (то есть веб-), он может состоять только из скомпилированной программы в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-118">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="7fcd7-119">Тем не менее типичный случай — это веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-119">However, the typical case is a Web-based application.</span></span></P>



<span data-ttu-id="7fcd7-120">Так как некоторые visual элемента управления, например сетки, флажок или список, может использовать возвращенных данных, возвращенных данных должен легко использовать visual элемент управления.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-120">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="7fcd7-121">Требуется простой и эффективный интерфейс программирования приложений, который поддерживает три уровня системы и возвращает сведения о качестве легко как если бы он был загружен на два уровня системы.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-121">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system.</span></span> <span data-ttu-id="7fcd7-122">Службы удаленных данных (RDS) — этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-122">Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="7fcd7-123">Решение</span><span class="sxs-lookup"><span data-stu-id="7fcd7-123">The Solution</span></span>

<span data-ttu-id="7fcd7-124">Определяет модель служб удаленных рабочих СТОЛОВ — последовательность действий, необходимых для получения доступа к и обновления в источнике данных, для получения доступа к данным через посредника, такие как Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="7fcd7-124">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="7fcd7-125">Модель программирования приведена сводка по всей функциональности RDS.</span><span class="sxs-lookup"><span data-stu-id="7fcd7-125">The programming model summarizes the entire functionality of RDS.</span></span>

