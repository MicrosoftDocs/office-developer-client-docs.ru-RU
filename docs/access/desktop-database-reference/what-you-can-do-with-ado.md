---
title: What You Can Do With ADO
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b7d0bab179cd7ec658bc04cee05f486947f38c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306022"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="853de-102">Что можно делать с помощью ADO</span><span class="sxs-lookup"><span data-stu-id="853de-102">What you can do with ADO</span></span>


<span data-ttu-id="853de-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="853de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="853de-104">ADO предоставляет разработчикам мощную логическую объектную модель для программного доступа, редактирования и обновления различных источников данных с помощью системных интерфейсов OLE DB.</span><span class="sxs-lookup"><span data-stu-id="853de-104">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces.</span></span> <span data-ttu-id="853de-105">Чаще всего ADO запрашивает таблицы или таблицы в реляционной базе данных, извлекает и отображает результаты в приложении, а также, возможно, позволяет пользователям вносить и сохранять изменения в данных.</span><span class="sxs-lookup"><span data-stu-id="853de-105">The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data.</span></span> <span data-ttu-id="853de-106">Кроме того, с помощью ADO можно программным путем:</span><span class="sxs-lookup"><span data-stu-id="853de-106">Other things that can be done programmatically with ADO include:</span></span>

- <span data-ttu-id="853de-107">Запрос базы данных с помощью SQL и отображение результатов.</span><span class="sxs-lookup"><span data-stu-id="853de-107">Querying a database using SQL and displaying the results.</span></span>

- <span data-ttu-id="853de-108">Доступ к сведениям в хранилище файлов через Интернет.</span><span class="sxs-lookup"><span data-stu-id="853de-108">Accessing information in a file store over the Internet.</span></span>

- <span data-ttu-id="853de-109">Управление сообщениями и папками в почтовой системе.</span><span class="sxs-lookup"><span data-stu-id="853de-109">Manipulating messages and folders in an email system.</span></span>

- <span data-ttu-id="853de-110">Сохранение данных из базы данных в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="853de-110">Saving data from a database into an XML file.</span></span>

- <span data-ttu-id="853de-111">Позволяет пользователю просмотреть и внести изменения в данные в таблицах баз данных.</span><span class="sxs-lookup"><span data-stu-id="853de-111">Allowing a user to review and make changes to data in database tables.</span></span>

- <span data-ttu-id="853de-112">Создание и повторное повторное создание параметровизованных команд базы данных.</span><span class="sxs-lookup"><span data-stu-id="853de-112">Creating and reusing parameterized database commands.</span></span>

- <span data-ttu-id="853de-113">Выполнение хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="853de-113">Executing stored procedures.</span></span>

- <span data-ttu-id="853de-114">Динамическое создание гибкой структуры, называемой **набором записей,** для хранения, навигации и управления данными.</span><span class="sxs-lookup"><span data-stu-id="853de-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

- <span data-ttu-id="853de-115">Выполнение транзакционной операции с базой данных.</span><span class="sxs-lookup"><span data-stu-id="853de-115">Performing transactional database operations.</span></span>

- <span data-ttu-id="853de-116">Фильтрация и сортировка локальных копий данных базы данных на основе критериев времени работы.</span><span class="sxs-lookup"><span data-stu-id="853de-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

- <span data-ttu-id="853de-117">Создание и управление иерархическими результатами из баз данных.</span><span class="sxs-lookup"><span data-stu-id="853de-117">Creating and manipulating hierarchical results from databases.</span></span>

- <span data-ttu-id="853de-118">Привязка полей базы данных к компонентам с данными.</span><span class="sxs-lookup"><span data-stu-id="853de-118">Binding database fields to data-aware components.</span></span>

- <span data-ttu-id="853de-119">Создание удаленных, отключенных **записей.**</span><span class="sxs-lookup"><span data-stu-id="853de-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="853de-120">ADO должен предоставлять широкий выбор параметров и параметров, чтобы обеспечить такую гибкость.</span><span class="sxs-lookup"><span data-stu-id="853de-120">ADO must expose a wide variety of options and settings in order to provide such flexibility.</span></span> <span data-ttu-id="853de-121">Поэтому важно использовать методический подход к использованию ADO в приложении, разбивая каждую из ваших целей на управляемые части.</span><span class="sxs-lookup"><span data-stu-id="853de-121">Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="853de-122">В большинстве программ ADO участвуют четыре основные операции: получение данных, изучение данных, изменение данных и обновление данных.</span><span class="sxs-lookup"><span data-stu-id="853de-122">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data.</span></span> <span data-ttu-id="853de-123">В следующих четырех главах каждая из этих операций рассматривается более подробно.</span><span class="sxs-lookup"><span data-stu-id="853de-123">The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="853de-124">Прежде чем перезапываться, ознакомьтесь с объектами в объектной модели ADO.</span><span class="sxs-lookup"><span data-stu-id="853de-124">Before proceeding, familiarize yourself with the objects in the ADO Object Model.</span></span> <span data-ttu-id="853de-125">Затем [просмотрите HelloData: простое приложение ADO.](hellodata-a-simple-ado-application.md)</span><span class="sxs-lookup"><span data-stu-id="853de-125">Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md).</span></span> <span data-ttu-id="853de-126">Это приложение написано на Visual Basic и выполняет каждую из четырех основных операций ADO.</span><span class="sxs-lookup"><span data-stu-id="853de-126">This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

