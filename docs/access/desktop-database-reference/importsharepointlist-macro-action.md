---
title: Действия макроса ImportSharePointList
TOCTitle: ImportSharePointList Macro Action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 57c6630b1e9145c158a32a331ae91157e8e5e8f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883073"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="20a6c-102">Действия макроса ImportSharePointList</span><span class="sxs-lookup"><span data-stu-id="20a6c-102">ImportSharePointList Macro Action</span></span>

<span data-ttu-id="20a6c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20a6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20a6c-104">Действие **ImportSharePointList** можно использовать для импорта данных с сайта Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="20a6c-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="20a6c-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="20a6c-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="setting"></a><span data-ttu-id="20a6c-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="20a6c-107">Setting</span></span>

<span data-ttu-id="20a6c-108">Действие **ImportSharePointList** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="20a6c-108">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20a6c-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="20a6c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="20a6c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="20a6c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-111"><strong>Тип передачи</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-111"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-112">Выберите тип переноса.</span><span class="sxs-lookup"><span data-stu-id="20a6c-112">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="20a6c-113">Выберите команду <strong>Импорт</strong> для копирования данных SharePoint Foundation в таблицу в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="20a6c-113">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="20a6c-114">Обновления данных в Access не влияют на данные в Windows SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="20a6c-114">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="20a6c-115">Аналогичным образом обновления данных в службах Windows SharePoint Services не влияют на данные в клиенте.</span><span class="sxs-lookup"><span data-stu-id="20a6c-115">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="20a6c-116">Выберите <strong>ссылку</strong> на создание связанной таблицы в Access для связи с данными в службах Windows SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="20a6c-116">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="20a6c-117">Обновление данных в Access, отражаются в Windows SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="20a6c-117">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="20a6c-118">Аналогичным образом обновления данных в службах Windows SharePoint Services, отражаются в клиенте.</span><span class="sxs-lookup"><span data-stu-id="20a6c-118">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-119"><strong>Адрес сайта</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-119"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-120">Введите полный путь на сайте SharePoint.</span><span class="sxs-lookup"><span data-stu-id="20a6c-120">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-121"><strong>Идентификатор списка</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-121"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-122">Введите имя или идентификатор GUID списка передачу.</span><span class="sxs-lookup"><span data-stu-id="20a6c-122">Enter the name or GUID of the list to be transferred.</span></span> <span data-ttu-id="20a6c-123">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="20a6c-123">Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-124"><strong>Идентификатор представления</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-124"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-125">Введите идентификатор GUID представления для списка, который требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="20a6c-125">Enter the GUID of the view for the list you want to use.</span></span> <span data-ttu-id="20a6c-126">Оставьте данный аргумент пустым, чтобы перенести все строки и столбцы в списке.</span><span class="sxs-lookup"><span data-stu-id="20a6c-126">Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20a6c-127"><strong>Имя таблицы</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-127"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-128">Введите имя, который будет отображаться для таблицы или связанной таблицы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="20a6c-128">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20a6c-129"><strong>Получить отображаемые значения подстановки</strong></span><span class="sxs-lookup"><span data-stu-id="20a6c-129"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="20a6c-130">Выберите <strong>Да</strong> , чтобы переключить отображаемые значения для поля подстановки, а не идентификатор, используемый для выполнения поиска.</span><span class="sxs-lookup"><span data-stu-id="20a6c-130">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="20a6c-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="20a6c-131">Remarks</span></span>

- <span data-ttu-id="20a6c-132">Это действие имеет тот же эффект, как нажатие **Списка SharePoint** в группу **импорта** на вкладке **Внешних данных** . Аргументы для действия соответствуют изменения, внесенные в мастере получение внешних данных.</span><span class="sxs-lookup"><span data-stu-id="20a6c-132">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="20a6c-133">Чтобы выполнить действие **ImportSharePointList** в модуле VBA, используйте метод **TransferSharePointList** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="20a6c-133">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="20a6c-134">Если указан несуществующий списка или представления, ошибка не происходит и данные не передаются.</span><span class="sxs-lookup"><span data-stu-id="20a6c-134">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="20a6c-135">GUID — это шестнадцатеричный уникальный идентификатор для списка или представления.</span><span class="sxs-lookup"><span data-stu-id="20a6c-135">A GUID is a unique hexadecimal identifier for a list or a view.</span></span> <span data-ttu-id="20a6c-136">Идентификатор GUID должен указываться в следующем формате, где каждый «F» — это шестнадцатеричный номер (0 до 9 или по F).</span><span class="sxs-lookup"><span data-stu-id="20a6c-136">A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="20a6c-137">Идентификатор GUID для списка или представления можно получить из сайта SharePoint с помощью следующей процедуры:</span><span class="sxs-lookup"><span data-stu-id="20a6c-137">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="20a6c-138">Откройте список в Windows SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="20a6c-138">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="20a6c-139">Если нужное представление не отображается, щелкните стрелку раскрывающегося списка **представления** и выберите нужное представление.</span><span class="sxs-lookup"><span data-stu-id="20a6c-139">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="20a6c-140">Щелкните стрелку раскрывающегося списка **представления** и выберите **изменить это представление**. Адрес в адресной строке браузера содержит идентификаторы GUID для списка и представления.</span><span class="sxs-lookup"><span data-stu-id="20a6c-140">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="20a6c-141">Исходя из GUID для списка **список =**, и идентификатор GUID для представления соответствует **представление =**.</span><span class="sxs-lookup"><span data-stu-id="20a6c-141">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="20a6c-142">Тем не менее, в поле адрес каждый символ **{** (левая фигурная скобка) представлены строки **% 7B**каждого **-** (дефис) представлены строка **% 2D**, и каждый символ **}** (закрывающая фигурная скобка) представлен строкой \*\* %7 D\*\*.</span><span class="sxs-lookup"><span data-stu-id="20a6c-142">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="20a6c-143">Пример:</span><span class="sxs-lookup"><span data-stu-id="20a6c-143">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="20a6c-144">Перед GUID с адреса, можно использовать в качестве аргументов в это действие макрос, необходимо заменить каждую строку, **% 7B** символ **{** , замените каждый **% 2D** строка с **-** символов и замените каждую строку **% 7 D** с символ **}** .</span><span class="sxs-lookup"><span data-stu-id="20a6c-144">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="20a6c-145">Не включать **&** () амперсанда, исходя из строки **% 7 D** в глобальный уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="20a6c-145">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

