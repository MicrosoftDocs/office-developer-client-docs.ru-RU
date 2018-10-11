---
title: 'Chapter 2: Getting Data'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d3df907e1dbe220caab58541b7c3eba605ef2f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481746"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="a1148-102">Chapter 2: Getting Data</span><span class="sxs-lookup"><span data-stu-id="a1148-102">Chapter 2: Getting Data</span></span>


<span data-ttu-id="a1148-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1148-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a1148-104">Предыдущей главе представлены четыре основных операций, используемых при создании приложения ADO: получение данных, анализ данных, изменение данных и обновление данных.</span><span class="sxs-lookup"><span data-stu-id="a1148-104">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data.</span></span> <span data-ttu-id="a1148-105">В этой главе нацеливаются на сведения о концепциях, имеющих отношение к первой операции: получение данных.</span><span class="sxs-lookup"><span data-stu-id="a1148-105">This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="a1148-106">Несколько объектов ADO можно играют роль в этой операции.</span><span class="sxs-lookup"><span data-stu-id="a1148-106">Several ADO objects can play a role in this operation.</span></span> <span data-ttu-id="a1148-107">Сначала подключиться к источнику данных с помощью объекта ADO- **подключение** (что иногда будут создаваться неявно).</span><span class="sxs-lookup"><span data-stu-id="a1148-107">First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly).</span></span> <span data-ttu-id="a1148-108">Затем передайте инструкции к источнику данных о требуется сделать с помощью объекта ADO **команды** (который также может быть создан неявно).</span><span class="sxs-lookup"><span data-stu-id="a1148-108">Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly).</span></span> <span data-ttu-id="a1148-109">В результате передачи команды к источнику данных и получения ответа обычно будут представлены в объект ADO **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a1148-109">The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="a1148-110">Для получения данных, приложения должны быть в связи с источником данных, например СУБД, хранилище файлов или файлов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="a1148-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="a1148-111">Эти подключения представляет *подключение* — среды, необходимые для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="a1148-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="a1148-112">Объектная модель ADO представляет концепцию соединение с объект **подключения** — foundation, на какие ADO построения функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="a1148-112">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built.</span></span> <span data-ttu-id="a1148-113">Объект **подключения** предназначен для:</span><span class="sxs-lookup"><span data-stu-id="a1148-113">The purpose of a **Connection** object is to:</span></span>

  - <span data-ttu-id="a1148-114">Определите сведения, необходимые ADO для взаимодействия с источниками данных и создание сеансов.</span><span class="sxs-lookup"><span data-stu-id="a1148-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

  - <span data-ttu-id="a1148-115">Определение возможности транзакций сеанса.</span><span class="sxs-lookup"><span data-stu-id="a1148-115">Define the transactional capabilities of the session.</span></span>

  - <span data-ttu-id="a1148-116">Дают возможность создания и выполнения команд в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="a1148-116">Allow you to create and execute commands against the data source.</span></span>

  - <span data-ttu-id="a1148-117">Представлены сведения о разработке источника данных в виде строк схемы.</span><span class="sxs-lookup"><span data-stu-id="a1148-117">Provide information about the design of the underlying data source in the form of schema rowsets.</span></span> <span data-ttu-id="a1148-118">Дополнительные сведения о наборах строк схемы [OpenSchema](openschema-method-ado.md)см.</span><span class="sxs-lookup"><span data-stu-id="a1148-118">For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

