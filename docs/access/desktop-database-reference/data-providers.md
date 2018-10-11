---
title: Поставщики данных (Справочник по для настольных баз данных Access)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd2f17bcc490031625cc8f6cd0ea6d369133fa06
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480630"
---
# <a name="data-providers"></a><span data-ttu-id="e38cc-102">Data Providers</span><span class="sxs-lookup"><span data-stu-id="e38cc-102">Data Providers</span></span>


<span data-ttu-id="e38cc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e38cc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e38cc-104">Поставщики данных представляют различных источников данных, таких как базы данных SQL, индексируются последовательных файлов, электронных таблиц, хранилищ документов и почты файлы.</span><span class="sxs-lookup"><span data-stu-id="e38cc-104">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files.</span></span> <span data-ttu-id="e38cc-105">Поставщики представление данных равномерно с помощью распространенных абстракции называется набор строк.</span><span class="sxs-lookup"><span data-stu-id="e38cc-105">Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="e38cc-106">ADO мощные и гибкие, так как он может подключиться к любой из нескольких разных поставщиков данных и по-прежнему предоставляют доступ к той же модели программирования, вне зависимости от конкретных компонентов любого заданного поставщика.</span><span class="sxs-lookup"><span data-stu-id="e38cc-106">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span> <span data-ttu-id="e38cc-107">Тем не менее так как каждый поставщик данных является уникальным, как приложение взаимодействует с ADO зависит от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="e38cc-107">However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="e38cc-108">К примеру возможности и функции поставщика OLE DB для SQL Server, который используется для доступа к базам данных Microsoft SQL Server, существенно отличаются от требований поставщик Microsoft OLE DB для публикации Интернета, который используется для доступа к файлу хранилища на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="e38cc-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a Web server.</span></span>

