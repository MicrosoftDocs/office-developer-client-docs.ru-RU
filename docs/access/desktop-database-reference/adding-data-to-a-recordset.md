---
title: Добавление данных в объект Recordset
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701398"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="42436-102">Добавление данных в объект Recordset</span><span class="sxs-lookup"><span data-stu-id="42436-102">Adding data to a Recordset</span></span>

<span data-ttu-id="42436-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42436-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42436-104">**Набор записей** представляет, вероятно, наиболее часто используемые объекты ADO.</span><span class="sxs-lookup"><span data-stu-id="42436-104">The **Recordset** is probably the most used of the ADO objects.</span></span> <span data-ttu-id="42436-105">В ADO **набор записей** — лучше всего считать как сочетание результирующий набор из источника данных и связанных с ним поведений.</span><span class="sxs-lookup"><span data-stu-id="42436-105">In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors.</span></span> <span data-ttu-id="42436-106">Таким образом можно размещения данных в **набор записей** и затем использовать для перемещения по строк данных, просмотр значений в строках и управлять результирующий набор **записей** методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="42436-106">Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="42436-107">В этом разделе нацеливаются на добавление данных в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="42436-107">This section will focus on adding data to the **Recordset**.</span></span> <span data-ttu-id="42436-108">Сведения о навигации по данных или обновления данных в разделе [раздел 4: редактирование данных](chapter-4-editing-data.md) и [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="42436-108">For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span> <span data-ttu-id="42436-109">Расширенные возможности объекта **команды** для добавления результирующий набор **записей**всегда нет необходимости.</span><span class="sxs-lookup"><span data-stu-id="42436-109">You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**.</span></span> <span data-ttu-id="42436-110">Часто следует выполнить команду путем установки свойства **источника** **записей** или передачи командной строки в метод **Open** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="42436-110">Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="42436-111">Существует несколько способов добавления данных из источника данных для **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="42436-111">There are a variety of ways to add data from your data source to a **Recordset**.</span></span> <span data-ttu-id="42436-112">Методики, которую вы используете зависит от требований приложения и возможности ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="42436-112">The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

