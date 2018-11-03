---
title: Что можно сделать с помощью ADO
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 02fd4c5dc5c44e15d8318653bbef9755899d61f6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947793"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="02ce1-102">Что можно сделать с помощью ADO</span><span class="sxs-lookup"><span data-stu-id="02ce1-102">What you can do with ADO</span></span>


<span data-ttu-id="02ce1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02ce1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02ce1-104">ADO предназначен для предоставления разработчикам мощные, логических объектной модели для программного доступа к, изменение и обновление широкий спектр источники данных через интерфейсы OLE DB системы.</span><span class="sxs-lookup"><span data-stu-id="02ce1-104">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces.</span></span> <span data-ttu-id="02ce1-105">Наиболее распространенные использования ADO является запрос таблицы или таблицы в реляционной базе данных, извлечения и отображения результатов в приложении и возможно разрешить пользователям одновременное внесение и сохранение изменений в данные.</span><span class="sxs-lookup"><span data-stu-id="02ce1-105">The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data.</span></span> <span data-ttu-id="02ce1-106">Другие действия, которые выполняются программным путем с помощью ADO включают:</span><span class="sxs-lookup"><span data-stu-id="02ce1-106">Other things that can be done programmatically with ADO include:</span></span>

  - <span data-ttu-id="02ce1-107">Запросы к базе данных с помощью SQL и отображения результатов.</span><span class="sxs-lookup"><span data-stu-id="02ce1-107">Querying a database using SQL and displaying the results.</span></span>

  - <span data-ttu-id="02ce1-108">Доступ к данным в хранилище файлов через Интернет.</span><span class="sxs-lookup"><span data-stu-id="02ce1-108">Accessing information in a file store over the Internet.</span></span>

  - <span data-ttu-id="02ce1-109">Управление файлами сообщений и папок в систему электронной почты.</span><span class="sxs-lookup"><span data-stu-id="02ce1-109">Manipulating messages and folders in an e-mail system.</span></span>

  - <span data-ttu-id="02ce1-110">Сохранение данных из базы данных в XML-файл.</span><span class="sxs-lookup"><span data-stu-id="02ce1-110">Saving data from a database into an XML file.</span></span>

  - <span data-ttu-id="02ce1-111">Позволяет пользователю для просмотра и изменения данных в таблицах базы данных.</span><span class="sxs-lookup"><span data-stu-id="02ce1-111">Allowing a user to review and make changes to data in database tables.</span></span>

  - <span data-ttu-id="02ce1-112">Создание и повторное использование параметризованные команды базы данных.</span><span class="sxs-lookup"><span data-stu-id="02ce1-112">Creating and reusing parameterized database commands.</span></span>

  - <span data-ttu-id="02ce1-113">Выполнение хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="02ce1-113">Executing stored procedures.</span></span>

  - <span data-ttu-id="02ce1-114">Динамическое создание гибкие структуры, называется набора **записей**, для хранения, перейдите и работы с данными.</span><span class="sxs-lookup"><span data-stu-id="02ce1-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

  - <span data-ttu-id="02ce1-115">Для выполнения операций транзакций базы данных.</span><span class="sxs-lookup"><span data-stu-id="02ce1-115">Performing transactional database operations.</span></span>

  - <span data-ttu-id="02ce1-116">Фильтрация и сортировка локальные копии сведения о базе данных на основе критериев во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="02ce1-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

  - <span data-ttu-id="02ce1-117">Создание и управление ими иерархических результаты из базы данных.</span><span class="sxs-lookup"><span data-stu-id="02ce1-117">Creating and manipulating hierarchical results from databases.</span></span>

  - <span data-ttu-id="02ce1-118">Привязка полей базы данных для данных компонентов.</span><span class="sxs-lookup"><span data-stu-id="02ce1-118">Binding database fields to data-aware components.</span></span>

  - <span data-ttu-id="02ce1-119">Создание удаленных, прервана **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="02ce1-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="02ce1-120">ADO должен предоставлять широкий набор параметров и настроек, чтобы обеспечить такую гибкость.</span><span class="sxs-lookup"><span data-stu-id="02ce1-120">ADO must expose a wide variety of options and settings in order to provide such flexibility.</span></span> <span data-ttu-id="02ce1-121">Поэтому важно выполнить тщательно, чтобы научиться использовать ADO в приложении, неудачного завершения каждого из выполнения задач на контролируемый части.</span><span class="sxs-lookup"><span data-stu-id="02ce1-121">Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="02ce1-122">Четыре основных операций участвуют в большинстве программ ADO: получение данных, анализ данных, изменение данных и обновление данных.</span><span class="sxs-lookup"><span data-stu-id="02ce1-122">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data.</span></span> <span data-ttu-id="02ce1-123">Следующие четыре главы проверьте каждой из этих операций, более подробно.</span><span class="sxs-lookup"><span data-stu-id="02ce1-123">The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="02ce1-124">Прежде чем продолжить, ознакомьтесь с объектами в объектной модели ADO.</span><span class="sxs-lookup"><span data-stu-id="02ce1-124">Before proceeding, familiarize yourself with the objects in the ADO Object Model.</span></span> <span data-ttu-id="02ce1-125">Просмотрите [HelloData: простое приложение ADO](hellodata-a-simple-ado-application.md).</span><span class="sxs-lookup"><span data-stu-id="02ce1-125">Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md).</span></span> <span data-ttu-id="02ce1-126">В этом приложении написаны в Visual Basic и выполняет каждого из четырех основных операций ADO.</span><span class="sxs-lookup"><span data-stu-id="02ce1-126">This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

