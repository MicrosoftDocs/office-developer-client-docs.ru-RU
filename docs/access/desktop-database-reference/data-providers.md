---
title: Поставщики данных (Справочник по для настольных баз данных Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc323161e2e97f34cab289430425958922f2406b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944433"
---
# <a name="data-providers"></a><span data-ttu-id="918b1-102">Поставщики данных</span><span class="sxs-lookup"><span data-stu-id="918b1-102">Data providers</span></span>


<span data-ttu-id="918b1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="918b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="918b1-104">Поставщики данных представляют различных источников данных, таких как базы данных SQL, индексируются последовательных файлов, электронных таблиц, хранилищ документов и почты файлы.</span><span class="sxs-lookup"><span data-stu-id="918b1-104">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files.</span></span> <span data-ttu-id="918b1-105">Поставщики представление данных равномерно с помощью распространенных абстракции называется набор строк.</span><span class="sxs-lookup"><span data-stu-id="918b1-105">Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="918b1-106">ADO мощные и гибкие, так как он может подключиться к любой из нескольких разных поставщиков данных и по-прежнему предоставляют доступ к той же модели программирования, вне зависимости от конкретных компонентов любого заданного поставщика.</span><span class="sxs-lookup"><span data-stu-id="918b1-106">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span> <span data-ttu-id="918b1-107">Тем не менее так как каждый поставщик данных является уникальным, как приложение взаимодействует с ADO зависит от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="918b1-107">However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="918b1-108">К примеру возможности и функции поставщика OLE DB для SQL Server, который используется для доступа к базам данных Microsoft SQL Server, существенно отличаются от требований поставщик Microsoft OLE DB для публикации Интернета, который используется для доступа к файлу хранилища на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="918b1-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a web server.</span></span>

