---
title: 'Глава 12: Учебник служб удаленных рабочих СТОЛОВ'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 276e8989b674c61414c42428bbff795bf700c6dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947681"
---
# <a name="chapter-12-rds-tutorial"></a><span data-ttu-id="a667d-102">Глава 12: Учебник служб удаленных рабочих СТОЛОВ</span><span class="sxs-lookup"><span data-stu-id="a667d-102">Chapter 12: RDS tutorial</span></span>

<span data-ttu-id="a667d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a667d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a667d-104">В этом руководстве описывается использование модели программирования служб удаленных рабочих СТОЛОВ для запроса и обновления в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="a667d-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="a667d-105">Во-первых описываются действия, необходимые для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="a667d-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="a667d-106">Затем учебника по повторяется в Microsoft Visual Basic Scripting Edition и Microsoft Visual J ++, продолжительностью ADO для Windows классов (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="a667d-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="a667d-107">В этом руководстве закодированные на разных языках по двум причинам:</span><span class="sxs-lookup"><span data-stu-id="a667d-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="a667d-108">В документации для служб удаленных рабочих СТОЛОВ предполагается коды чтения в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a667d-108">The documentation for RDS assumes the reader codes in Visual Basic.</span></span> <span data-ttu-id="a667d-109">Это делает документации удобным для программистов Visual Basic, но меньше полезен для программистов, использовать другие языки.</span><span class="sxs-lookup"><span data-stu-id="a667d-109">This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="a667d-110">Если вы не уверены в определенный компонент служб удаленных рабочих СТОЛОВ и вам известно немного из другой язык, может иметь возможность сопоставлять вопрос, используя для одного компонента выразить на другом языке.</span><span class="sxs-lookup"><span data-stu-id="a667d-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

## <a name="how-the-tutorial-is-presented"></a><span data-ttu-id="a667d-111">Как представлены учебника по</span><span class="sxs-lookup"><span data-stu-id="a667d-111">How the tutorial is presented</span></span>

<span data-ttu-id="a667d-112">В этом руководстве основано на модели программирования служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="a667d-112">This tutorial is based on the RDS programming model.</span></span> <span data-ttu-id="a667d-113">По отдельности рассматривается каждый шаг модели программирования.</span><span class="sxs-lookup"><span data-stu-id="a667d-113">It discusses each step of the programming model individually.</span></span> <span data-ttu-id="a667d-114">Кроме того показан фрагмент кода Visual Basic по каждому шагу.</span><span class="sxs-lookup"><span data-stu-id="a667d-114">In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="a667d-115">В примере кода повторяется на других языках с минимальными обсуждений.</span><span class="sxs-lookup"><span data-stu-id="a667d-115">The code example is repeated in other languages with minimal discussion.</span></span> <span data-ttu-id="a667d-116">Каждый шаг в учебном курсе заданного языка программирования в модель программирования и описания при помощи учебника по помечен соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="a667d-116">Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial.</span></span> <span data-ttu-id="a667d-117">Используйте номер шага для ссылки на обсуждения в описательное учебном курсе.</span><span class="sxs-lookup"><span data-stu-id="a667d-117">Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="a667d-118">Модель программирования служб удаленных рабочих СТОЛОВ указанное ниже.</span><span class="sxs-lookup"><span data-stu-id="a667d-118">The RDS programming model is stated below.</span></span> <span data-ttu-id="a667d-119">Используйте его в качестве руководства, как во время выполнения учебника по.</span><span class="sxs-lookup"><span data-stu-id="a667d-119">Use it as a roadmap as you proceed through the tutorial.</span></span>

## <a name="rds-programming-model-with-objects"></a><span data-ttu-id="a667d-120">Модель программирования служб удаленных рабочих СТОЛОВ с объектами</span><span class="sxs-lookup"><span data-stu-id="a667d-120">RDS programming model with objects</span></span>

- <span data-ttu-id="a667d-121">Укажите программу для вызова на сервере и получить способом (прокси-сервер), обратитесь к нему из клиента.</span><span class="sxs-lookup"><span data-stu-id="a667d-121">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="a667d-122">Вызов программы сервера.</span><span class="sxs-lookup"><span data-stu-id="a667d-122">Invoke the server program.</span></span> <span data-ttu-id="a667d-123">Передайте параметры программы сервера, которое идентифицирует источник данных и команды для выдачи.</span><span class="sxs-lookup"><span data-stu-id="a667d-123">Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="a667d-124">Программы сервера получает объект [набора записей](recordset-object-ado.md) из источника данных, обычно с помощью ADO.</span><span class="sxs-lookup"><span data-stu-id="a667d-124">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO.</span></span> <span data-ttu-id="a667d-125">Кроме того в объект **набора записей** обрабатывается на сервере.</span><span class="sxs-lookup"><span data-stu-id="a667d-125">Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="a667d-126">Программы сервера возвращает окончательный объекта **набора записей** для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="a667d-126">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="a667d-127">В клиенте объекта **набора записей** при необходимости поместите в форму, можно легко использовать визуальные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="a667d-127">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="a667d-128">Изменения в объект **набора записей** отправляются на сервер и используется для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="a667d-128">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

<span data-ttu-id="a667d-129">Ниже перечислены действия, описанные в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="a667d-129">Following are the steps in this tutorial:</span></span>

- [<span data-ttu-id="a667d-130">Шаг 1: Укажите программы сервера</span><span class="sxs-lookup"><span data-stu-id="a667d-130">Step 1: Specify a server program</span></span>](step-1-specify-a-server-program-rds-tutorial.md)
- [<span data-ttu-id="a667d-131">Шаг 2: Вызова программы сервера</span><span class="sxs-lookup"><span data-stu-id="a667d-131">Step 2: Invoke the server program</span></span>](step-2-invoke-the-server-program-rds-tutorial.md)
- [<span data-ttu-id="a667d-132">Шаг 3: Сервер получает набор записей</span><span class="sxs-lookup"><span data-stu-id="a667d-132">Step 3: Server obtains a Recordset</span></span>](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [<span data-ttu-id="a667d-133">Шаг 4: Сервер возвращает набор записей</span><span class="sxs-lookup"><span data-stu-id="a667d-133">Step 4: Server returns the Recordset</span></span>](step-4-server-returns-the-recordset-rds-tutorial.md)
- [<span data-ttu-id="a667d-134">Шаг 5: DataControl сделано могут использоваться</span><span class="sxs-lookup"><span data-stu-id="a667d-134">Step 5: DataControl is made usable</span></span>](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [<span data-ttu-id="a667d-135">Шаг 6: Изменения отправляются на сервер</span><span class="sxs-lookup"><span data-stu-id="a667d-135">Step 6: Changes are sent to the server</span></span>](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [<span data-ttu-id="a667d-136">При помощи учебника по служб удаленных рабочих СТОЛОВ (VBScript)</span><span class="sxs-lookup"><span data-stu-id="a667d-136">RDS tutorial (VBScript)</span></span>](rds-tutorial-vbscript.md)
- [<span data-ttu-id="a667d-137">При помощи учебника по служб удаленных рабочих СТОЛОВ (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="a667d-137">RDS tutorial (Visual J++)</span></span>](rds-tutorial-visual-j.md)