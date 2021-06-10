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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280218"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="03766-102">Добавление данных в объект Recordset</span><span class="sxs-lookup"><span data-stu-id="03766-102">Adding data to a Recordset</span></span>

<span data-ttu-id="03766-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03766-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03766-104">**Recordset,** вероятно, является наиболее используемым из объектов ADO.</span><span class="sxs-lookup"><span data-stu-id="03766-104">The **Recordset** is probably the most used of the ADO objects.</span></span> <span data-ttu-id="03766-105">В ADO **recordset** лучше всего подумать как сочетание результата, задаваемого источником данных, и связанных с ним поведения курсоров.</span><span class="sxs-lookup"><span data-stu-id="03766-105">In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors.</span></span> <span data-ttu-id="03766-106">Таким образом, можно поместить данные в **набор Recordset,** а затем использовать методы и свойства **Recordset** для навигации по строкам данных, просмотра значений в строках и иного манипулирования набором результатов.</span><span class="sxs-lookup"><span data-stu-id="03766-106">Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="03766-107">В этом разделе основное внимание будет уделяться добавлению данных в **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="03766-107">This section will focus on adding data to the **Recordset**.</span></span> <span data-ttu-id="03766-108">Сведения о навигации по данным или обновлении данных см. в главе [4. Редактирование](chapter-4-editing-data.md) данных и глава [5: обновление и обновление данных.](chapter-5-updating-and-persisting-data.md)</span><span class="sxs-lookup"><span data-stu-id="03766-108">For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span> <span data-ttu-id="03766-109">Для добавления набора результатов в набор  Recordset не всегда требуются расширенные возможности объекта **Command.**</span><span class="sxs-lookup"><span data-stu-id="03766-109">You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**.</span></span> <span data-ttu-id="03766-110">Часто можно выполнить команду, задав свойство **Source** в **наборе Recordset** или передав строку команды объекту **Recordset** **Open.**</span><span class="sxs-lookup"><span data-stu-id="03766-110">Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="03766-111">Существует множество способов добавления данных из источника данных в **набор Recordset.**</span><span class="sxs-lookup"><span data-stu-id="03766-111">There are a variety of ways to add data from your data source to a **Recordset**.</span></span> <span data-ttu-id="03766-112">Используемая методика зависит от потребностей приложения и возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="03766-112">The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

