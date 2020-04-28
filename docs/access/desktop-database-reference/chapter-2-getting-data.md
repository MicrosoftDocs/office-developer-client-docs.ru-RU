---
title: Глава 2. Получение данных
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f059e5dfe064442f10972fd36344e64f84fe7ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296446"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="3b16b-102">Глава 2. Получение данных</span><span class="sxs-lookup"><span data-stu-id="3b16b-102">Chapter 2: Getting data</span></span>

<span data-ttu-id="3b16b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b16b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b16b-104">Предыдущая глава предоставила четыре основных операции, которые используются при создании приложения ADO: извлечение данных, изучение данных, редактирование данных и обновление данных.</span><span class="sxs-lookup"><span data-stu-id="3b16b-104">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data.</span></span> <span data-ttu-id="3b16b-105">В этой главе рассматриваются сведения о концепциях, связанных с первой операцией: получения данных.</span><span class="sxs-lookup"><span data-stu-id="3b16b-105">This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="3b16b-106">В этой операции может воспроизводиться несколько объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="3b16b-106">Several ADO objects can play a role in this operation.</span></span> <span data-ttu-id="3b16b-107">Сначала подключитесь к источнику данных с помощью объекта **подключения** ADO (который иногда создается неявным образом).</span><span class="sxs-lookup"><span data-stu-id="3b16b-107">First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly).</span></span> <span data-ttu-id="3b16b-108">Затем вы передаете инструкции источнику данных о том, что нужно сделать с помощью объекта **команды** ADO (который также можно создать неявно).</span><span class="sxs-lookup"><span data-stu-id="3b16b-108">Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly).</span></span> <span data-ttu-id="3b16b-109">Результат передачи команды источнику данных и получения его ответа обычно будет представлен в объекте **Recordset** объекта ADO.</span><span class="sxs-lookup"><span data-stu-id="3b16b-109">The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="3b16b-110">Для получения данных ваше приложение должно находиться в связи с источником данных, таким как СУБД, хранилищем файлов или текстовым файлом, разделенным запятыми.</span><span class="sxs-lookup"><span data-stu-id="3b16b-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="3b16b-111">Это взаимодействие представляет собой *Подключение* — среду, необходимую для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="3b16b-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="3b16b-112">Объектная модель ADO представляет концепцию подключения с помощью объекта **Connection** — фундамента, на котором создаются многие функциональные возможности ADO.</span><span class="sxs-lookup"><span data-stu-id="3b16b-112">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built.</span></span> <span data-ttu-id="3b16b-113">Объект **Connection** предназначен для:</span><span class="sxs-lookup"><span data-stu-id="3b16b-113">The purpose of a **Connection** object is to:</span></span>

- <span data-ttu-id="3b16b-114">Определение сведений, необходимых ADO для связи с источниками данных и создания сеансов.</span><span class="sxs-lookup"><span data-stu-id="3b16b-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

- <span data-ttu-id="3b16b-115">Определите возможности сеанса для транзакций.</span><span class="sxs-lookup"><span data-stu-id="3b16b-115">Define the transactional capabilities of the session.</span></span>

- <span data-ttu-id="3b16b-116">Позволяет создавать и выполнять команды для источника данных.</span><span class="sxs-lookup"><span data-stu-id="3b16b-116">Allow you to create and execute commands against the data source.</span></span>

- <span data-ttu-id="3b16b-117">Предоставьте сведения о структуре базового источника данных в виде наборов строк схемы.</span><span class="sxs-lookup"><span data-stu-id="3b16b-117">Provide information about the design of the underlying data source in the form of schema rowsets.</span></span> <span data-ttu-id="3b16b-118">Дополнительные сведения о наборах строк схемы приведены в разделе [метод OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3b16b-118">For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="3b16b-119">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="3b16b-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="3b16b-120">Создание подключения</span><span class="sxs-lookup"><span data-stu-id="3b16b-120">Making a connection</span></span>](making-a-connection.md)
- [<span data-ttu-id="3b16b-121">Использование ссылки на объект Connection (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b16b-121">Using the connection object reference (ADO)</span></span>](using-the-connection-object-access.md)
- [<span data-ttu-id="3b16b-122">Использование справочника по объекту Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b16b-122">Using the command object reference (ADO)</span></span>](using-the-command-object-access.md)
- [<span data-ttu-id="3b16b-123">Добавление данных в объект Recordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b16b-123">Adding data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)
