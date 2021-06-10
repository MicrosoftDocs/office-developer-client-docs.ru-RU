---
title: Поставщики данных (ссылка на настольные базы данных)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 46d9cf80bfdd15f48d876fe63a617c9b30931fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295067"
---
# <a name="data-providers"></a><span data-ttu-id="bc330-102">Поставщики данных</span><span class="sxs-lookup"><span data-stu-id="bc330-102">Data providers</span></span>


<span data-ttu-id="bc330-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc330-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc330-104">Поставщики данных представляют различные источники данных, такие как SQL базы данных, индексные-последовательное файлы, электронные таблицы, хранилища документов и почтовые файлы.</span><span class="sxs-lookup"><span data-stu-id="bc330-104">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files.</span></span> <span data-ttu-id="bc330-105">Поставщики подвергают данные равномерно, используя общую абстракцию под названием rowset.</span><span class="sxs-lookup"><span data-stu-id="bc330-105">Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="bc330-106">ADO является мощным и гибким, поскольку он может подключаться к любому из нескольких различных поставщиков данных и по-прежнему выставлять ту же модель программирования, независимо от конкретных функций того или иного поставщика.</span><span class="sxs-lookup"><span data-stu-id="bc330-106">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span> <span data-ttu-id="bc330-107">Однако, поскольку каждый поставщик данных уникален, взаимодействие приложения с ADO зависит от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="bc330-107">However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="bc330-108">Например, возможности и возможности поставщика OLE DB для SQL Server, который используется для доступа к базам данных Microsoft SQL Server, значительно отличаются от возможностей поставщика DB Microsoft OLE для интернет-публикации, который используется для доступа к хранилищам файлов на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="bc330-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a web server.</span></span>

