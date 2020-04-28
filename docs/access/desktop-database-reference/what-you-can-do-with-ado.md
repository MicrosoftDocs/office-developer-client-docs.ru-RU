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
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="b4e2e-102">Что можно делать с помощью ADO</span><span class="sxs-lookup"><span data-stu-id="b4e2e-102">What you can do with ADO</span></span>


<span data-ttu-id="b4e2e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4e2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4e2e-104">ADO предоставляет разработчикам мощную логическую объектную модель для программного доступа, редактирования и обновления разнообразных источников данных с помощью системных интерфейсов OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-104">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces.</span></span> <span data-ttu-id="b4e2e-105">Наиболее распространенный способ использования ADO — запрос таблицы или таблиц в реляционной базе данных, извлечение и отображение результатов в приложении и, возможно, предоставление пользователям возможности вносить и сохранять изменения данных.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-105">The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data.</span></span> <span data-ttu-id="b4e2e-106">Ниже перечислены другие возможности, которые можно выполнять программным способом с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-106">Other things that can be done programmatically with ADO include:</span></span>

- <span data-ttu-id="b4e2e-107">Запрос к базе данных с помощью SQL и отображение результатов.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-107">Querying a database using SQL and displaying the results.</span></span>

- <span data-ttu-id="b4e2e-108">Доступ к данным в хранилище файлов через Интернет.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-108">Accessing information in a file store over the Internet.</span></span>

- <span data-ttu-id="b4e2e-109">Управление сообщениями и папками в почтовой системе.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-109">Manipulating messages and folders in an email system.</span></span>

- <span data-ttu-id="b4e2e-110">Сохранение данных из базы данных в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-110">Saving data from a database into an XML file.</span></span>

- <span data-ttu-id="b4e2e-111">Разрешение пользователям просматривать и вносить изменения в данные в таблицах базы данных.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-111">Allowing a user to review and make changes to data in database tables.</span></span>

- <span data-ttu-id="b4e2e-112">Создание и повторное использование параметризованных команд базы данных.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-112">Creating and reusing parameterized database commands.</span></span>

- <span data-ttu-id="b4e2e-113">Выполнение хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-113">Executing stored procedures.</span></span>

- <span data-ttu-id="b4e2e-114">Динамическое создание гибкой структуры, называемой **набором записей**, для хранения, навигации и управления данными.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

- <span data-ttu-id="b4e2e-115">Выполнение транзакционных операций базы данных.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-115">Performing transactional database operations.</span></span>

- <span data-ttu-id="b4e2e-116">Фильтрация и сортировка локальных копий данных базы данных на основе критериев времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

- <span data-ttu-id="b4e2e-117">Создание иерархических результатов из баз данных и управление ими.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-117">Creating and manipulating hierarchical results from databases.</span></span>

- <span data-ttu-id="b4e2e-118">Привязка полей базы данных к компонентам, поддерживающим данные.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-118">Binding database fields to data-aware components.</span></span>

- <span data-ttu-id="b4e2e-119">Создание удаленных, отключенных **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="b4e2e-120">Для обеспечения такой гибкости в ADO должны быть предоставлены разнообразные параметры и настройки.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-120">ADO must expose a wide variety of options and settings in order to provide such flexibility.</span></span> <span data-ttu-id="b4e2e-121">Поэтому важно принять методичномуный подход к изучению использования ADO в приложении, разбивая каждую из ваших целей на управляемые части.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-121">Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="b4e2e-122">В большинстве программ ADO используются четыре основных операции: извлечение данных, анализ данных, редактирование данных и обновление данных.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-122">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data.</span></span> <span data-ttu-id="b4e2e-123">В следующих четырех главах каждая из этих операций рассматривается более подробно.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-123">The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="b4e2e-124">Прежде чем продолжить, ознакомьтесь с объектами в объектной модели ADO.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-124">Before proceeding, familiarize yourself with the objects in the ADO Object Model.</span></span> <span data-ttu-id="b4e2e-125">Проверьте [HelloData: простое приложение ADO](hellodata-a-simple-ado-application.md).</span><span class="sxs-lookup"><span data-stu-id="b4e2e-125">Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md).</span></span> <span data-ttu-id="b4e2e-126">Это приложение написано в Visual Basic и выполняет каждую из четырех основных операций ADO.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-126">This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

