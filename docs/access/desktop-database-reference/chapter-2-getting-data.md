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
# <a name="chapter-2-getting-data"></a><span data-ttu-id="2c1f7-102">Глава 2. Получение данных</span><span class="sxs-lookup"><span data-stu-id="2c1f7-102">Chapter 2: Getting data</span></span>

<span data-ttu-id="2c1f7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c1f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c1f7-104">В предыдущей главе представлены четыре основные операции, связанные с созданием приложения ADO: получение данных, изучение данных, изменение данных и обновление данных.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-104">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data.</span></span> <span data-ttu-id="2c1f7-105">В этой главе основное внимание будет уделяться концепциям, относянымся к первой операции: получение данных.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-105">This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="2c1f7-106">Несколько объектов ADO могут играть определенную роль в этой операции.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-106">Several ADO objects can play a role in this operation.</span></span> <span data-ttu-id="2c1f7-107">Сначала необходимо подключиться к источнику данных с помощью объекта подключения **ADO** (который иногда создается неявно).</span><span class="sxs-lookup"><span data-stu-id="2c1f7-107">First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly).</span></span> <span data-ttu-id="2c1f7-108">Затем вы передаете в источник данных инструкции о том, что нужно сделать с помощью объекта команды **ADO** (который также можно создать неявно).</span><span class="sxs-lookup"><span data-stu-id="2c1f7-108">Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly).</span></span> <span data-ttu-id="2c1f7-109">Результат передачи команды в источник данных и получения ее ответа обычно будет представлен в объекте ADO **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="2c1f7-109">The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="2c1f7-110">Чтобы получить данные, приложение должно быть в связи с источником данных, таким как DBMS, хранилище файлов или текстовый файл с запятой.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="2c1f7-111">Это сообщение представляет собой *подключение —* среду, необходимую для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="2c1f7-112">Объектная модель ADO представляет концепцию подключения к объекту **Connection** — основа, на которой построена функциональность ADO.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-112">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built.</span></span> <span data-ttu-id="2c1f7-113">Объект **Connection** предназначен для:</span><span class="sxs-lookup"><span data-stu-id="2c1f7-113">The purpose of a **Connection** object is to:</span></span>

- <span data-ttu-id="2c1f7-114">Определите сведения, необходимые ADO для связи с источниками данных, и создайте сеансы.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

- <span data-ttu-id="2c1f7-115">Определите транзакционные возможности сеанса.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-115">Define the transactional capabilities of the session.</span></span>

- <span data-ttu-id="2c1f7-116">Позволяет создавать и выполнять команды для источника данных.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-116">Allow you to create and execute commands against the data source.</span></span>

- <span data-ttu-id="2c1f7-117">Предоставление сведений о проектировании источника данных в форме наборов строк схемы.</span><span class="sxs-lookup"><span data-stu-id="2c1f7-117">Provide information about the design of the underlying data source in the form of schema rowsets.</span></span> <span data-ttu-id="2c1f7-118">Дополнительные сведения о строках схемы см. в [методе OpenSchema.](openschema-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="2c1f7-118">For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="2c1f7-119">В этой главе освещались следующие темы:</span><span class="sxs-lookup"><span data-stu-id="2c1f7-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="2c1f7-120">Создание подключения</span><span class="sxs-lookup"><span data-stu-id="2c1f7-120">Making a connection</span></span>](making-a-connection.md)
- [<span data-ttu-id="2c1f7-121">Using the connection object reference (ADO)</span><span class="sxs-lookup"><span data-stu-id="2c1f7-121">Using the connection object reference (ADO)</span></span>](using-the-connection-object-access.md)
- [<span data-ttu-id="2c1f7-122">Using the command object reference (ADO)</span><span class="sxs-lookup"><span data-stu-id="2c1f7-122">Using the command object reference (ADO)</span></span>](using-the-command-object-access.md)
- [<span data-ttu-id="2c1f7-123">Добавление данных в набор recordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="2c1f7-123">Adding data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)
