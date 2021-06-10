---
title: Макрокоманда ImportSharePointList
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291861"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="102b0-102">Макрокоманда ImportSharePointList</span><span class="sxs-lookup"><span data-stu-id="102b0-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="102b0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="102b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="102b0-104">Вы можете использовать **действие ImportSharePointList** для импорта или ссылки данных с сайта Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="102b0-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="102b0-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="102b0-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="102b0-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="102b0-106">Setting</span></span>

<span data-ttu-id="102b0-107">Действие **ImportSharePointList** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="102b0-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="102b0-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="102b0-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="102b0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="102b0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="102b0-110"><strong>Тип преобразования</strong></span><span class="sxs-lookup"><span data-stu-id="102b0-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="102b0-111">Выберите тип переноса.</span><span class="sxs-lookup"><span data-stu-id="102b0-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="102b0-112">Выберите <strong>Импорт</strong> для копирования данных SharePoint Foundation в таблицу в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="102b0-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="102b0-113">Обновления данных в Access не влияют на данные в SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="102b0-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="102b0-114">Кроме того, обновления данных в SharePoint Foundation не влияют на данные в Access.</span><span class="sxs-lookup"><span data-stu-id="102b0-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="102b0-115">Выберите <strong>Ссылку</strong> для создания связанной таблицы в Access, которая связывается с данными в SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="102b0-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="102b0-116">Обновления данных в Access отражены в SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="102b0-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="102b0-117">Кроме того, обновления данных в SharePoint Foundation отражаются в Access.</span><span class="sxs-lookup"><span data-stu-id="102b0-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="102b0-118"><strong>Адрес сайта</strong></span><span class="sxs-lookup"><span data-stu-id="102b0-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="102b0-119">Введите полный путь SharePoint сайта.</span><span class="sxs-lookup"><span data-stu-id="102b0-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="102b0-120"><strong>ID списка</strong></span><span class="sxs-lookup"><span data-stu-id="102b0-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="102b0-121">Введите имя или GUID перенаправленного списка.</span><span class="sxs-lookup"><span data-stu-id="102b0-121">Enter the name or GUID of the list to be transferred.</span></span> <span data-ttu-id="102b0-122">Необходимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="102b0-122">Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="102b0-123"><strong>Просмотр ID</strong></span><span class="sxs-lookup"><span data-stu-id="102b0-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="102b0-124">Введите GUID представления для списка, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="102b0-124">Enter the GUID of the view for the list you want to use.</span></span> <span data-ttu-id="102b0-125">Оставьте этот аргумент пустым, чтобы перенести все строки и столбцы в списке.</span><span class="sxs-lookup"><span data-stu-id="102b0-125">Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="102b0-126"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="102b0-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="102b0-127">Введите имя, отображаемую для таблицы или связанной таблицы в Access.</span><span class="sxs-lookup"><span data-stu-id="102b0-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="102b0-128"><strong>Получить значения отображения lookup</strong></span><span class="sxs-lookup"><span data-stu-id="102b0-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="102b0-129">Выберите <strong>Да</strong> для переноса значений отображения полей Lookup вместо ID, используемого для выполнения отображения.</span><span class="sxs-lookup"><span data-stu-id="102b0-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="102b0-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="102b0-130">Remarks</span></span>

- <span data-ttu-id="102b0-131">Это действие имеет такой же эффект, как SharePoint **список** в группе **Импорт** на вкладке **Внешние** данные. Аргументы для действия соответствуют решениям, которые вы делаете в мастере внешних данных Get.</span><span class="sxs-lookup"><span data-stu-id="102b0-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="102b0-132">Чтобы выполнить **действие ImportSharePointList** в модуле VBA, используйте метод **TransferSharePointList** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="102b0-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="102b0-133">При указании несущестуго списка или представления ошибки не происходит и данные не передаются.</span><span class="sxs-lookup"><span data-stu-id="102b0-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="102b0-134">GUID — уникальный идентификатор hexadecimal для списка или представления.</span><span class="sxs-lookup"><span data-stu-id="102b0-134">A GUID is a unique hexadecimal identifier for a list or a view.</span></span> <span data-ttu-id="102b0-135">GUID должен быть введен в следующем формате, где каждый "F" является гексадецимальным номером (от 0 до 9 или A через F).</span><span class="sxs-lookup"><span data-stu-id="102b0-135">A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="102b0-136">Вы можете получить GUID для списка или представления с сайта SharePoint с помощью следующей процедуры:</span><span class="sxs-lookup"><span data-stu-id="102b0-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="102b0-137">Откройте список в SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="102b0-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="102b0-138">Если нужное представление не отображается, щелкните стрелку **представления,** а затем выберите нужное представление.</span><span class="sxs-lookup"><span data-stu-id="102b0-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="102b0-139">Щелкните **стрелку "Просмотр",** а затем выберите **Изменение этого представления.** Адрес в панели адресов браузера содержит GUID-коды как для списка, так и для представления.</span><span class="sxs-lookup"><span data-stu-id="102b0-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="102b0-140">GUID для списка следует **List=** и GUID для представления следует **View=**.</span><span class="sxs-lookup"><span data-stu-id="102b0-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="102b0-141">Однако в адресе каждый **символ {(левая** скобка) представлен строкой **%7B,** каждый символ (дефис) представлен строкой **-** **%2D,** а каждый **символ }** (справа скобка) представлен строкой **%7D**.</span><span class="sxs-lookup"><span data-stu-id="102b0-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="102b0-142">Пример.</span><span class="sxs-lookup"><span data-stu-id="102b0-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="102b0-143">Прежде чем использовать GUID-интерфейсы из адреса в качестве аргументов в этом макросовом действии, необходимо заменить каждую строку **%7B** на **{character,** заменить каждую строку **%2D** на символ и заменить каждую **-** **строку %7D** на **}.**</span><span class="sxs-lookup"><span data-stu-id="102b0-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="102b0-144">Не включите **&** символ (ampersand), который следует **строке %7D** в GUID списка.</span><span class="sxs-lookup"><span data-stu-id="102b0-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

