---
title: Решения для удаленного доступа к данным
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b64ed19c268874e0e52a87bc2e05aacb6083422
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306904"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="08ceb-102">Решения для удаленного доступа к данным</span><span class="sxs-lookup"><span data-stu-id="08ceb-102">Solutions for Remote Data Access</span></span>

<span data-ttu-id="08ceb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08ceb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="08ceb-104">Проблема</span><span class="sxs-lookup"><span data-stu-id="08ceb-104">The issue</span></span>

<span data-ttu-id="08ceb-105">ADO позволяет приложению напрямую получать доступ к источникам данных и изменять их (иногда это называется двухуровневой системой).</span><span class="sxs-lookup"><span data-stu-id="08ceb-105">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system).</span></span> <span data-ttu-id="08ceb-106">Например, если подключение к источнику данных содержит данные, это прямое подключение в двухуровневой системе.</span><span class="sxs-lookup"><span data-stu-id="08ceb-106">For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="08ceb-107">Однако может потребоваться косвенное доступ к источникам данных через посредника, например Microsoft IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="08ceb-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="08ceb-108">Это расположение иногда называется трехуровневой системой.</span><span class="sxs-lookup"><span data-stu-id="08ceb-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="08ceb-109">IIS — это клиентская или серверная система, которая обеспечивает эффективный способ для локального или клиентского приложения вызывать удаленную или серверную программу через Интернет или интрасеть.</span><span class="sxs-lookup"><span data-stu-id="08ceb-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="08ceb-110">Серверная программа получает доступ к источнику данных и необязательным образом обрабатывает приобретенные данные.</span><span class="sxs-lookup"><span data-stu-id="08ceb-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="08ceb-111">Например, веб-сайт интрасети содержит приложение, написанное в Microsoft Visual Basic Scripting Edition (VBScript), которое подключается к IIS.</span><span class="sxs-lookup"><span data-stu-id="08ceb-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="08ceb-112">IIS в свою очередь подключается к фактическому источнику данных, извлекает данные, обрабатывает их каким-то образом, а затем возвращает обработанные сведения в ваше приложение.</span><span class="sxs-lookup"><span data-stu-id="08ceb-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="08ceb-113">В этом примере приложение никогда напрямую не подключено к источнику данных; IIS сделал.</span><span class="sxs-lookup"><span data-stu-id="08ceb-113">In this example, your application never directly connected to the data source; IIS did.</span></span> <span data-ttu-id="08ceb-114">И IIS получили доступ к данным с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="08ceb-114">And IIS accessed the data by means of ADO.</span></span>

> [!NOTE]
> <span data-ttu-id="08ceb-115">Клиент/серверное приложение не должно основываться на Интернете или интрасети (то есть на веб-основе) — оно может состоять исключительно из компиляции программ в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="08ceb-115">The client/server application does not have to be based on the Internet or an intranet (that is, web-based)—it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="08ceb-116">Однако типичным случаем является веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="08ceb-116">However, the typical case is a web-based application.</span></span>

<span data-ttu-id="08ceb-117">Поскольку некоторые визуальные функции управления, такие как сетка, контрольное окно или список, могут использовать возвращаемую информацию, возвращаемая информация должна быть легко использована визуальным управлением.</span><span class="sxs-lookup"><span data-stu-id="08ceb-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="08ceb-118">Требуется простой и эффективный интерфейс программирования приложений, который поддерживает трехуровневые системы и возвращает информацию так же легко, как если бы она была извлечена в двухуровневой системе.</span><span class="sxs-lookup"><span data-stu-id="08ceb-118">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system.</span></span> <span data-ttu-id="08ceb-119">Удаленные службы данных (RDS) это интерфейс.</span><span class="sxs-lookup"><span data-stu-id="08ceb-119">Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="08ceb-120">Решение</span><span class="sxs-lookup"><span data-stu-id="08ceb-120">The solution</span></span>

<span data-ttu-id="08ceb-121">RDS определяет модель программирования — последовательность действий, необходимых для получения доступа к источнику данных и обновления, для получения доступа к данным через посредника, например службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="08ceb-121">RDS defines a programming model—the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="08ceb-122">Модель программирования обобщает всю функциональность RDS.</span><span class="sxs-lookup"><span data-stu-id="08ceb-122">The programming model summarizes the entire functionality of RDS.</span></span>

