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
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="210c6-102">HelloData: простое приложение ADO</span><span class="sxs-lookup"><span data-stu-id="210c6-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="210c6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="210c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="210c6-104">Чтобы заложить основу для изучения библиотеки ADO, рассмотрите простое приложение ADO под названием "HelloData".</span><span class="sxs-lookup"><span data-stu-id="210c6-104">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData."</span></span> <span data-ttu-id="210c6-105">HelloData по шагам в каждой из четырех основных операций ADO (получение, изучение, редактирование и обновление данных).</span><span class="sxs-lookup"><span data-stu-id="210c6-105">HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data).</span></span> <span data-ttu-id="210c6-106">Чтобы сосредоточиться на основах ADO и предотвратить помехи в коде, в примере делается минимальная обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="210c6-106">In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="210c6-107">Приложение запрашивает пример базы данных Northwind, включаемую в Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="210c6-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="210c6-108">**Запуск HelloData**</span><span class="sxs-lookup"><span data-stu-id="210c6-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="210c6-109">Создайте новый стандартный исполняемый Visual Basic Project, который ссылается на библиотеку ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="210c6-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="210c6-110">Создайте четыре кнопки команд в верхней части формы, установив для свойств **Name** и **Caption** значения, показанные в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="210c6-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="210c6-111">Под кнопками добавьте microsoft **DataGrid Control** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="210c6-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="210c6-112">Файл Msdatgrd.ocx поставляется с Visual Basic и находится в каталоге \\ Windows \\ system32 или \\ winnt \\ system32.</span><span class="sxs-lookup"><span data-stu-id="210c6-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="210c6-113">Чтобы добавить элемент управления DataGrid в Visual Basic панели элементов, выберите "Компоненты"... в меню **"Проект".** </span><span class="sxs-lookup"><span data-stu-id="210c6-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="210c6-114">Затем пойдите в поле "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" и нажмите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="210c6-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="210c6-115">Чтобы добавить этот контроль в проект, перетащите его с панели инструментов на Visual Basic формы.</span><span class="sxs-lookup"><span data-stu-id="210c6-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="210c6-116">Создайте **TextBox** на форме под сеткой и задайте его свойства, как показано в таблице.</span><span class="sxs-lookup"><span data-stu-id="210c6-116">Create a **TextBox** on the form below the grid and set its properties as shown in the table.</span></span> <span data-ttu-id="210c6-117">По завершению форма должна выглядеть примерно так, как на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="210c6-117">The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="210c6-118">Наконец, скопируйте код, указанный в [коде HelloData,](hellodata-code.md) и в paste его в окне редактора кода формы.</span><span class="sxs-lookup"><span data-stu-id="210c6-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="210c6-119">Нажмите **F5,** чтобы запустить код.</span><span class="sxs-lookup"><span data-stu-id="210c6-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="210c6-120">В следующем примере и во всем руководстве для проверки подлинности на сервере используется код MyId с паролем "123aBc".</span><span class="sxs-lookup"><span data-stu-id="210c6-120">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="210c6-121">Эти значения следует заменить действительными учетными данными для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="210c6-121">You should substitute these values with valid logon credentials for your server.</span></span> <span data-ttu-id="210c6-122">Кроме того, замените значение MyServer именем сервера.</span><span class="sxs-lookup"><span data-stu-id="210c6-122">Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="210c6-123">Подробное описание кода см. в описании [HelloData Details.](hellodata-details.md)</span><span class="sxs-lookup"><span data-stu-id="210c6-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="210c6-124">Тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="210c6-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="210c6-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="210c6-125">Property</span></span></p></th>
<th><p><span data-ttu-id="210c6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="210c6-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="210c6-127">Form</span><span class="sxs-lookup"><span data-stu-id="210c6-127">Form</span></span></p></td>
<td><p><span data-ttu-id="210c6-128">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-128">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-129">Form1</span><span class="sxs-lookup"><span data-stu-id="210c6-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-130">Height</span><span class="sxs-lookup"><span data-stu-id="210c6-130">Height</span></span></p></td>
<td><p><span data-ttu-id="210c6-131">6500</span><span class="sxs-lookup"><span data-stu-id="210c6-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-132">Width</span><span class="sxs-lookup"><span data-stu-id="210c6-132">Width</span></span></p></td>
<td><p><span data-ttu-id="210c6-133">6500</span><span class="sxs-lookup"><span data-stu-id="210c6-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="210c6-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="210c6-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="210c6-135">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-135">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="210c6-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210c6-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="210c6-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="210c6-138">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-138">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="210c6-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-140">Многолинейная</span><span class="sxs-lookup"><span data-stu-id="210c6-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="210c6-141">true</span><span class="sxs-lookup"><span data-stu-id="210c6-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210c6-142">Кнопка команды</span><span class="sxs-lookup"><span data-stu-id="210c6-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="210c6-143">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-143">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="210c6-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-145">Подпись</span><span class="sxs-lookup"><span data-stu-id="210c6-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="210c6-146">Получить данные</span><span class="sxs-lookup"><span data-stu-id="210c6-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210c6-147">Кнопка команды</span><span class="sxs-lookup"><span data-stu-id="210c6-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="210c6-148">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-148">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="210c6-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-150">Подпись</span><span class="sxs-lookup"><span data-stu-id="210c6-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="210c6-151">Изучение данных</span><span class="sxs-lookup"><span data-stu-id="210c6-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210c6-152">Кнопка команды</span><span class="sxs-lookup"><span data-stu-id="210c6-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="210c6-153">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-153">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="210c6-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-155">Подпись</span><span class="sxs-lookup"><span data-stu-id="210c6-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="210c6-156">Изменение данных</span><span class="sxs-lookup"><span data-stu-id="210c6-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="210c6-157">Кнопка команды</span><span class="sxs-lookup"><span data-stu-id="210c6-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="210c6-158">Имя</span><span class="sxs-lookup"><span data-stu-id="210c6-158">Name</span></span></p></td>
<td><p><span data-ttu-id="210c6-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="210c6-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="210c6-160">Подпись</span><span class="sxs-lookup"><span data-stu-id="210c6-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="210c6-161">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="210c6-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



