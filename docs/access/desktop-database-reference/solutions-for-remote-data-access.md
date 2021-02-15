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
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="1c0c5-102">Решения для удаленного доступа к данным</span><span class="sxs-lookup"><span data-stu-id="1c0c5-102">Solutions for Remote Data Access</span></span>

<span data-ttu-id="1c0c5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c0c5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="1c0c5-104">Проблема</span><span class="sxs-lookup"><span data-stu-id="1c0c5-104">The issue</span></span>

<span data-ttu-id="1c0c5-105">ADO позволяет приложению напрямую получать доступ к источникам данных и изменять их (иногда называемую двухуровневой системой).</span><span class="sxs-lookup"><span data-stu-id="1c0c5-105">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system).</span></span> <span data-ttu-id="1c0c5-106">Например, если вы подключены к источнику данных, который содержит ваши данные, это прямое подключение в двухуровневой системе.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-106">For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="1c0c5-107">Однако может потребоваться косвенный доступ к источникам данных через посредника, например Microsoft IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="1c0c5-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="1c0c5-108">Такое расположение иногда называется трехуровневой системой.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="1c0c5-109">IIS — это клиент/серверная система, которая обеспечивает эффективный способ вызова удаленной программой или сервером в Интернете или интрасети локальным приложением или клиентом.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="1c0c5-110">Серверная программа получает доступ к источнику данных и при желании обрабатывает полученные данные.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="1c0c5-111">Например, ваша веб-страницу интрасети содержит приложение, написанное в Microsoft Visual Basic Scripting Edition (VBScript), которое подключается к IIS.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="1c0c5-112">IiS, в свою очередь, подключается к фактическому источнику данных, извлекает данные, обрабатывает их каким-либо образом, а затем возвращает обработанные сведения в приложение.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="1c0c5-113">В этом примере приложение никогда не подключается напрямую к источнику данных; IiS.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-113">In this example, your application never directly connected to the data source; IIS did.</span></span> <span data-ttu-id="1c0c5-114">И IIS доступ к данным с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-114">And IIS accessed the data by means of ADO.</span></span>

> [!NOTE]
> <span data-ttu-id="1c0c5-115">Клиент/серверное приложение не должно быть основано на Интернете или интрасети (то есть на веб-сайте) — оно может состоять исключительно из скомпилализованных программ в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-115">The client/server application does not have to be based on the Internet or an intranet (that is, web-based)—it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="1c0c5-116">Однако типичным случаем является веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-116">However, the typical case is a web-based application.</span></span>

<span data-ttu-id="1c0c5-117">Так как некоторые визуальные функции управления, такие как сетка, контрольный список или список, могут использовать возвращаемую информацию, возвращаемая информация должна быть легко использована визуальным управлением.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="1c0c5-118">Вам нужен простой и эффективный интерфейс программирования приложений, который поддерживает трехуровневые системы и возвращает сведения так же легко, как если бы они были извлечены в двухуровневой системе.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-118">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system.</span></span> <span data-ttu-id="1c0c5-119">Это интерфейс удаленной службы данных (RDS).</span><span class="sxs-lookup"><span data-stu-id="1c0c5-119">Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="1c0c5-120">Решение</span><span class="sxs-lookup"><span data-stu-id="1c0c5-120">The solution</span></span>

<span data-ttu-id="1c0c5-121">RDS определяет модель программирования ( последовательность действий, необходимых для получения доступа к источнику данных и обновления) для получения доступа к данным через посредника, например служб IIS.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-121">RDS defines a programming model—the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="1c0c5-122">Модель программирования объединяет все функциональные возможности RDS.</span><span class="sxs-lookup"><span data-stu-id="1c0c5-122">The programming model summarizes the entire functionality of RDS.</span></span>

