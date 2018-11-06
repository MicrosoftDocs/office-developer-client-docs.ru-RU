---
title: 'HelloData: Простого ADO приложения'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 359816f828191a8643941a21ac520ba7b3231e6b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998205"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="0bb5f-102">HelloData: Простого ADO приложения</span><span class="sxs-lookup"><span data-stu-id="0bb5f-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="0bb5f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bb5f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0bb5f-104">Чтобы подготовиться к просмотра библиотеки ADO, рассмотрим простое приложение ADO называется «HelloData».</span><span class="sxs-lookup"><span data-stu-id="0bb5f-104">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData."</span></span> <span data-ttu-id="0bb5f-105">HelloData шаги по каждой из четырех основных операций ADO (начало, проверки, изменение и обновление данных).</span><span class="sxs-lookup"><span data-stu-id="0bb5f-105">HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data).</span></span> <span data-ttu-id="0bb5f-106">Чтобы сосредоточиться на основ ADO и избежать лишних кода, обработка ошибок минимальной выполняется в примере.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-106">In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="0bb5f-107">Приложение запрашивает образце базы данных Northwind, который входит в состав Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="0bb5f-108">**Для запуска HelloData**</span><span class="sxs-lookup"><span data-stu-id="0bb5f-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="0bb5f-109">Создание нового проекта Visual Basic стандартный исполняемый файл, который ссылается ADO 2.5 библиотеки.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="0bb5f-110">Создайте четыре командные кнопки в верхней части формы, установка для свойства **Name** и **Caption** значения, указанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="0bb5f-111">Ниже кнопок добавьте элемент **Управления DataGrid Microsoft** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="0bb5f-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="0bb5f-112">Файл Msdatgrd.ocx, поступающие с помощью Visual Basic и находится в вашей \\windows\\system32 или \\winnt\\каталог system32.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="0bb5f-113">Чтобы добавить элемент управления DataGrid в область элементов Visual Basic, выберите **компоненты...** в меню **проект** .</span><span class="sxs-lookup"><span data-stu-id="0bb5f-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="0bb5f-114">Затем установите флажок рядом с элементом «элемент управления DataGrid Microsoft 6.0 (SP3) (OLEDB)» и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="0bb5f-115">Чтобы добавить элемент управления в проект, перетащите элемент управления DataGrid из панели элементов Visual Basic форму.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="0bb5f-116">Создание **текстового поля** на форме под сетку и задайте его свойства, как показано в таблице.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-116">Create a **TextBox** on the form below the grid and set its properties as shown in the table.</span></span> <span data-ttu-id="0bb5f-117">Формы должен выглядеть на следующем рисунке, после завершения.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-117">The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="0bb5f-118">И, наконец скопируйте код, приведенный в [HelloData код](hellodata-code.md) и вставьте его в окно редактора кода формы.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="0bb5f-119">Нажмите клавишу **F5** , чтобы запустить код.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="0bb5f-120">В следующем примере и в руководстве идентификатор пользователя «Мой_идентификатор» пароль «123aBc» используется для проверки подлинности на сервере.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-120">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="0bb5f-121">Необходимо заменить эти значения с действительные учетные данные для сервера.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-121">You should substitute these values with valid logon credentials for your server.</span></span> <span data-ttu-id="0bb5f-122">Кроме того замените «MyServer» значение с именем сервера.</span><span class="sxs-lookup"><span data-stu-id="0bb5f-122">Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="0bb5f-123">Подробное описание код ознакомиться с [Подробными сведениями HelloData](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="0bb5f-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bb5f-124">Тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="0bb5f-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="0bb5f-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="0bb5f-125">Property</span></span></p></th>
<th><p><span data-ttu-id="0bb5f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0bb5f-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bb5f-127">Form</span><span class="sxs-lookup"><span data-stu-id="0bb5f-127">Form</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-128">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-128">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-129">Form1</span><span class="sxs-lookup"><span data-stu-id="0bb5f-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-130">Height</span><span class="sxs-lookup"><span data-stu-id="0bb5f-130">Height</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-131">6500</span><span class="sxs-lookup"><span data-stu-id="0bb5f-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-132">Width</span><span class="sxs-lookup"><span data-stu-id="0bb5f-132">Width</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-133">6500</span><span class="sxs-lookup"><span data-stu-id="0bb5f-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bb5f-134">DataGrid мс</span><span class="sxs-lookup"><span data-stu-id="0bb5f-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-135">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-135">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="0bb5f-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bb5f-137">Текстовое поле</span><span class="sxs-lookup"><span data-stu-id="0bb5f-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-138">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-138">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="0bb5f-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="0bb5f-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-141">true</span><span class="sxs-lookup"><span data-stu-id="0bb5f-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bb5f-142">Кнопки</span><span class="sxs-lookup"><span data-stu-id="0bb5f-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-143">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-143">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="0bb5f-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-145">Caption</span><span class="sxs-lookup"><span data-stu-id="0bb5f-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-146">Получение данных</span><span class="sxs-lookup"><span data-stu-id="0bb5f-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bb5f-147">Кнопки</span><span class="sxs-lookup"><span data-stu-id="0bb5f-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-148">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-148">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="0bb5f-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-150">Caption</span><span class="sxs-lookup"><span data-stu-id="0bb5f-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-151">Проверка данных</span><span class="sxs-lookup"><span data-stu-id="0bb5f-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bb5f-152">Кнопки</span><span class="sxs-lookup"><span data-stu-id="0bb5f-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-153">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-153">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="0bb5f-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-155">Caption</span><span class="sxs-lookup"><span data-stu-id="0bb5f-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-156">Изменение данных</span><span class="sxs-lookup"><span data-stu-id="0bb5f-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bb5f-157">Кнопки</span><span class="sxs-lookup"><span data-stu-id="0bb5f-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-158">Имя</span><span class="sxs-lookup"><span data-stu-id="0bb5f-158">Name</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="0bb5f-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="0bb5f-160">Caption</span><span class="sxs-lookup"><span data-stu-id="0bb5f-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="0bb5f-161">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="0bb5f-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



