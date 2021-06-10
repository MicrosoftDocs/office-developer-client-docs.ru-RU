---
title: 'HelloData: простое приложение ADO'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292022"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="3c1c4-102">HelloData: простое приложение ADO</span><span class="sxs-lookup"><span data-stu-id="3c1c4-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="3c1c4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c1c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c1c4-104">Чтобы заложить основу для исследования библиотеки ADO, рассмотрим простое приложение ADO под названием "HelloData".</span><span class="sxs-lookup"><span data-stu-id="3c1c4-104">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData."</span></span> <span data-ttu-id="3c1c4-105">HelloData проходит каждую из четырех основных операций ADO (получение, изучение, редактирование и обновление данных).</span><span class="sxs-lookup"><span data-stu-id="3c1c4-105">HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data).</span></span> <span data-ttu-id="3c1c4-106">Чтобы сосредоточиться на основах ADO и предотвратить захламленность кода, в примере делается минимальная обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-106">In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="3c1c4-107">Приложение запрашивает примерную базу данных Northwind, включенную в Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="3c1c4-108">**Запуск HelloData**</span><span class="sxs-lookup"><span data-stu-id="3c1c4-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="3c1c4-109">Создайте новый стандартный Visual Basic Project, который ссылается на библиотеку ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="3c1c4-110">Создайте четыре кнопки команд в верхней части формы, установив свойства **Name** и **Caption** к значениям, показанным в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="3c1c4-111">Ниже кнопок добавьте **microsoft DataGrid Control** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="3c1c4-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="3c1c4-112">Файл Msdatgrd.ocx поставляется с Visual Basic и расположен в каталоге \\ windows \\ system32 или \\ winnt \\ system32.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="3c1c4-113">Чтобы добавить элемент управления DataGrid в Visual Basic панели инструментов, выберите **компоненты...** из **Project** меню.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="3c1c4-114">Затем проверьте поле рядом с "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="3c1c4-115">Чтобы добавить управление в проект, перетащите управление DataGrid из панели инструментов в форму Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="3c1c4-116">Создайте **TextBox** на форме ниже сетки и задайте ее свойства, как показано в таблице.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-116">Create a **TextBox** on the form below the grid and set its properties as shown in the table.</span></span> <span data-ttu-id="3c1c4-117">Форма должна выглядеть аналогично следующей фигуре по завершению.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-117">The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="3c1c4-118">Наконец, скопируйте код, указанный в [Коде HelloData,](hellodata-code.md) и вклеите его в окно редактора кода формы.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="3c1c4-119">Нажмите **кнопку F5** для запуска кода.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="3c1c4-120">В следующем примере и во всем руководстве для проверки подлинности на сервере используется пользовательский id "MyId" с паролем "123aBc".</span><span class="sxs-lookup"><span data-stu-id="3c1c4-120">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="3c1c4-121">Эти значения следует заменить действительными учетными данными с логотипом для сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-121">You should substitute these values with valid logon credentials for your server.</span></span> <span data-ttu-id="3c1c4-122">Кроме того, замените значение "MyServer" именем сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1c4-122">Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="3c1c4-123">Подробные сведения о коде см. в [материале HelloData Details.](hellodata-details.md)</span><span class="sxs-lookup"><span data-stu-id="3c1c4-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c1c4-124">Тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="3c1c4-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="3c1c4-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="3c1c4-125">Property</span></span></p></th>
<th><p><span data-ttu-id="3c1c4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3c1c4-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c1c4-127">Form</span><span class="sxs-lookup"><span data-stu-id="3c1c4-127">Form</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-128">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-128">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-129">Form1</span><span class="sxs-lookup"><span data-stu-id="3c1c4-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-130">Height</span><span class="sxs-lookup"><span data-stu-id="3c1c4-130">Height</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-131">6500</span><span class="sxs-lookup"><span data-stu-id="3c1c4-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-132">Width</span><span class="sxs-lookup"><span data-stu-id="3c1c4-132">Width</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-133">6500</span><span class="sxs-lookup"><span data-stu-id="3c1c4-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c1c4-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="3c1c4-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-135">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-135">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="3c1c4-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c1c4-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="3c1c4-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-138">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-138">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="3c1c4-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="3c1c4-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-141">true</span><span class="sxs-lookup"><span data-stu-id="3c1c4-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c1c4-142">Кнопка Командная</span><span class="sxs-lookup"><span data-stu-id="3c1c4-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-143">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-143">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="3c1c4-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-145">Подпись</span><span class="sxs-lookup"><span data-stu-id="3c1c4-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="3c1c4-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c1c4-147">Кнопка Командная</span><span class="sxs-lookup"><span data-stu-id="3c1c4-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-148">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-148">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="3c1c4-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-150">Подпись</span><span class="sxs-lookup"><span data-stu-id="3c1c4-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-151">Изучение данных</span><span class="sxs-lookup"><span data-stu-id="3c1c4-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c1c4-152">Кнопка Командная</span><span class="sxs-lookup"><span data-stu-id="3c1c4-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-153">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-153">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="3c1c4-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-155">Подпись</span><span class="sxs-lookup"><span data-stu-id="3c1c4-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-156">Изменение данных</span><span class="sxs-lookup"><span data-stu-id="3c1c4-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c1c4-157">Кнопка Командная</span><span class="sxs-lookup"><span data-stu-id="3c1c4-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-158">Name</span><span class="sxs-lookup"><span data-stu-id="3c1c4-158">Name</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="3c1c4-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="3c1c4-160">Подпись</span><span class="sxs-lookup"><span data-stu-id="3c1c4-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="3c1c4-161">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="3c1c4-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



