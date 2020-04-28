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
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="03b88-102">HelloData: простое приложение ADO</span><span class="sxs-lookup"><span data-stu-id="03b88-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="03b88-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03b88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03b88-104">Чтобы создать основу для исследования библиотеки ADO, рассмотрим простое приложение ADO под названием "HelloData".</span><span class="sxs-lookup"><span data-stu-id="03b88-104">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData."</span></span> <span data-ttu-id="03b88-105">HelloData пошаговые инструкции по каждой из четырех основных операций ADO (знакомство, просмотр, редактирование и обновление данных).</span><span class="sxs-lookup"><span data-stu-id="03b88-105">HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data).</span></span> <span data-ttu-id="03b88-106">Чтобы сосредоточиться на основных понятиях ADO и предотвратить несрочный код, в этом примере выполняется минимальная обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="03b88-106">In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="03b88-107">Приложение запрашивает учебную базу данных Northwind, которая входит в состав Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="03b88-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="03b88-108">**Запуск HelloData**</span><span class="sxs-lookup"><span data-stu-id="03b88-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="03b88-109">Создайте новый стандартный исполняемый проект Visual Basic, который ссылается на библиотеку ADO 2,5.</span><span class="sxs-lookup"><span data-stu-id="03b88-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="03b88-110">Создайте четыре кнопки в верхней части формы, задав для свойств **Name** и **Caption** значения, указанные в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="03b88-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="03b88-111">Под кнопками добавьте **элемент управления Microsoft DataGrid** (мсдатгрд. ocx).</span><span class="sxs-lookup"><span data-stu-id="03b88-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="03b88-112">Файл Мсдатгрд. ocx поставляется с Visual Basic и находится в \\каталоге Windows\\System32 или \\WinNT\\System32.</span><span class="sxs-lookup"><span data-stu-id="03b88-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="03b88-113">Чтобы добавить элемент управления DataGrid на панель элементов Visual Basic, выберите **компоненты...** в меню **проект** .</span><span class="sxs-lookup"><span data-stu-id="03b88-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="03b88-114">Затем установите флажок "элемент управления Microsoft DataGrid 6,0 (с пакетом обновления 3) (OLEDB)" и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="03b88-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="03b88-115">Чтобы добавить элемент управления в проект, перетащите элемент управления DataGrid из панели элементов в форму Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="03b88-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="03b88-116">Создайте **текстовое поле** в форме под сеткой и задайте его свойства, как показано в таблице.</span><span class="sxs-lookup"><span data-stu-id="03b88-116">Create a **TextBox** on the form below the grid and set its properties as shown in the table.</span></span> <span data-ttu-id="03b88-117">По завершении форма должна выглядеть примерно так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="03b88-117">The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="03b88-118">Наконец, скопируйте код, приведенный в [HelloData Code](hellodata-code.md) , и вставьте его в окно редактора кода формы.</span><span class="sxs-lookup"><span data-stu-id="03b88-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="03b88-119">Нажмите клавишу **F5** , чтобы запустить код.</span><span class="sxs-lookup"><span data-stu-id="03b88-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="03b88-120">В приведенном ниже примере и в рамках руководства для проверки подлинности на сервере используется идентификатор пользователя "MyId" с паролем "123aBc".</span><span class="sxs-lookup"><span data-stu-id="03b88-120">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server.</span></span> <span data-ttu-id="03b88-121">Необходимо заменить эти значения действительными учетными данными для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="03b88-121">You should substitute these values with valid logon credentials for your server.</span></span> <span data-ttu-id="03b88-122">Кроме того, замените "MyServer" на имя вашего сервера.</span><span class="sxs-lookup"><span data-stu-id="03b88-122">Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="03b88-123">Подробное описание кода приведено в разделе [HelloData Details](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="03b88-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03b88-124">Тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="03b88-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="03b88-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="03b88-125">Property</span></span></p></th>
<th><p><span data-ttu-id="03b88-126">Значение</span><span class="sxs-lookup"><span data-stu-id="03b88-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b88-127">Форма</span><span class="sxs-lookup"><span data-stu-id="03b88-127">Form</span></span></p></td>
<td><p><span data-ttu-id="03b88-128">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-128">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-129">Form1</span><span class="sxs-lookup"><span data-stu-id="03b88-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-130">Height</span><span class="sxs-lookup"><span data-stu-id="03b88-130">Height</span></span></p></td>
<td><p><span data-ttu-id="03b88-131">6500</span><span class="sxs-lookup"><span data-stu-id="03b88-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-132">Width</span><span class="sxs-lookup"><span data-stu-id="03b88-132">Width</span></span></p></td>
<td><p><span data-ttu-id="03b88-133">6500</span><span class="sxs-lookup"><span data-stu-id="03b88-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b88-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="03b88-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="03b88-135">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-135">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="03b88-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b88-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="03b88-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="03b88-138">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-138">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="03b88-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-140">Скидок</span><span class="sxs-lookup"><span data-stu-id="03b88-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="03b88-141">true</span><span class="sxs-lookup"><span data-stu-id="03b88-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b88-142">Кнопка</span><span class="sxs-lookup"><span data-stu-id="03b88-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="03b88-143">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-143">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-144">кмджетдата</span><span class="sxs-lookup"><span data-stu-id="03b88-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-145">Подпись</span><span class="sxs-lookup"><span data-stu-id="03b88-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="03b88-146">Получение данных</span><span class="sxs-lookup"><span data-stu-id="03b88-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b88-147">Кнопка</span><span class="sxs-lookup"><span data-stu-id="03b88-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="03b88-148">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-148">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-149">кмдексаминедата</span><span class="sxs-lookup"><span data-stu-id="03b88-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-150">Подпись</span><span class="sxs-lookup"><span data-stu-id="03b88-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="03b88-151">Анализ данных</span><span class="sxs-lookup"><span data-stu-id="03b88-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b88-152">Кнопка</span><span class="sxs-lookup"><span data-stu-id="03b88-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="03b88-153">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-153">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-154">кмдедитдата</span><span class="sxs-lookup"><span data-stu-id="03b88-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-155">Подпись</span><span class="sxs-lookup"><span data-stu-id="03b88-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="03b88-156">Изменение данных</span><span class="sxs-lookup"><span data-stu-id="03b88-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b88-157">Кнопка</span><span class="sxs-lookup"><span data-stu-id="03b88-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="03b88-158">Имя</span><span class="sxs-lookup"><span data-stu-id="03b88-158">Name</span></span></p></td>
<td><p><span data-ttu-id="03b88-159">кмдупдатедата</span><span class="sxs-lookup"><span data-stu-id="03b88-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="03b88-160">Подпись</span><span class="sxs-lookup"><span data-stu-id="03b88-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="03b88-161">Обновление данных</span><span class="sxs-lookup"><span data-stu-id="03b88-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



