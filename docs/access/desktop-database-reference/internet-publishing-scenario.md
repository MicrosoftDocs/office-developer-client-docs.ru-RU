---
title: Сценарий публикации в Интернете
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026451"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="832ce-102">Сценарий публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="832ce-102">Internet publishing scenario</span></span>

<span data-ttu-id="832ce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="832ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="832ce-104">В этом примере кода показано, как использовать ADO с поставщик Microsoft OLE DB для публикации Интернет.</span><span class="sxs-lookup"><span data-stu-id="832ce-104">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="832ce-105">В данном сценарии создается приложения Visual Basic, использующего объекты **набора записей**, **записи**и **поток** для отображения содержимого из ресурсов, опубликованные с поставщиком публикации Интернет.</span><span class="sxs-lookup"><span data-stu-id="832ce-105">In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="832ce-106">Для создания этого сценария необходимы следующие действия:</span><span class="sxs-lookup"><span data-stu-id="832ce-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="832ce-107">Настройка проекта Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="832ce-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="832ce-108">Инициализируйте поле со списком Main.</span><span class="sxs-lookup"><span data-stu-id="832ce-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="832ce-109">Заполните поля.</span><span class="sxs-lookup"><span data-stu-id="832ce-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="832ce-110">Заполните текстовое поле сведений.</span><span class="sxs-lookup"><span data-stu-id="832ce-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="832ce-111">Этап 1: Настройка проекта Visual Basic</span><span class="sxs-lookup"><span data-stu-id="832ce-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="832ce-112">В этом сценарии предполагается, что у вас есть Microsoft Visual Basic 6.0 или более поздней версии, ADO 2.5 или более поздней версии и поставщик Microsoft OLE DB для публикации Интернет в системе.</span><span class="sxs-lookup"><span data-stu-id="832ce-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="832ce-113">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="832ce-113">Create an ADO project</span></span>

1.  <span data-ttu-id="832ce-114">В Microsoft Visual Basic, создайте новый проект стандартный exe-ФАЙЛ.</span><span class="sxs-lookup"><span data-stu-id="832ce-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="832ce-115">В меню **проект** выберите команду **Справочные материалы**.</span><span class="sxs-lookup"><span data-stu-id="832ce-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="832ce-116">Выберите **Библиотеку 2.5 объекты данных ActiveX Microsoft**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="832ce-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="832ce-117">Вставка элементов управления в форме</span><span class="sxs-lookup"><span data-stu-id="832ce-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="832ce-118">Добавьте в форму Form1 элемент управления ListBox.</span><span class="sxs-lookup"><span data-stu-id="832ce-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="832ce-119">Установите для свойства **имя** **lstMain**.</span><span class="sxs-lookup"><span data-stu-id="832ce-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="832ce-120">Добавьте другой элемент управления ListBox Form1.</span><span class="sxs-lookup"><span data-stu-id="832ce-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="832ce-121">Установите для свойства **имя** **lstDetails**.</span><span class="sxs-lookup"><span data-stu-id="832ce-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="832ce-122">Добавьте элемент управления TextBox в форму Form1.</span><span class="sxs-lookup"><span data-stu-id="832ce-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="832ce-123">Установите для свойства **имя** **txtDetails**.</span><span class="sxs-lookup"><span data-stu-id="832ce-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="832ce-124">Шаг 2: Инициализировать поле со списком Main</span><span class="sxs-lookup"><span data-stu-id="832ce-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="832ce-125">Объявите глобальные объекты набора записей и записи</span><span class="sxs-lookup"><span data-stu-id="832ce-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="832ce-126">Вставьте следующий код в (Общие) (раздел описаний) для Form1:</span><span class="sxs-lookup"><span data-stu-id="832ce-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="832ce-127">Этот код объявляет ссылки на глобальный объект для объектов **записи** и **записей** , которые будут использоваться позже в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="832ce-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="832ce-128">Подключение к URL-адрес и заполнения lstMain</span><span class="sxs-lookup"><span data-stu-id="832ce-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="832ce-129">Вставьте следующий код в обработчик событий загрузки формы для Form1:</span><span class="sxs-lookup"><span data-stu-id="832ce-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   <span data-ttu-id="832ce-130">Этот код создает глобальные объекты **набора записей** и **записи** .</span><span class="sxs-lookup"><span data-stu-id="832ce-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="832ce-131">**Запись** `grec` открывается с URL-адрес, указанный в качестве **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="832ce-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="832ce-132">Если существует URL-адрес, он открывается; Если он еще не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="832ce-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="832ce-133">Обратите внимание, что необходимо заменить `https://servername/foldername/` с допустимый URL-адрес из среды.</span><span class="sxs-lookup"><span data-stu-id="832ce-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="832ce-134">**Набор записей** `grs` открывается на дочерних элементов **записи** `grec`.</span><span class="sxs-lookup"><span data-stu-id="832ce-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="832ce-135">Затем lstMain заполняется имена файлов ресурсов, опубликованные в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="832ce-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="832ce-136">Шаг 3: Заполнения списка полей</span><span class="sxs-lookup"><span data-stu-id="832ce-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="832ce-137">Вставьте следующий код в обработчик событий Click lstMain:</span><span class="sxs-lookup"><span data-stu-id="832ce-137">Insert the following code into the Click event handler of lstMain:</span></span>

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   <span data-ttu-id="832ce-138">Этот код объявляет и создает локальные объекты **набора записей** и **записи** `rec` и `rs`соответственно.</span><span class="sxs-lookup"><span data-stu-id="832ce-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="832ce-139">Строку, соответствующую ресурсов, выбранных в lstMain будет создано текущей строки `grs`.</span><span class="sxs-lookup"><span data-stu-id="832ce-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="832ce-140">**Сведения о** списке затем флажка и `rec` открывается с текущей строки `grs` как источник.</span><span class="sxs-lookup"><span data-stu-id="832ce-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="832ce-141">Если ресурс коллекцию записи (в соответствии с **типом записи**), локального **набора записей** `rs` открывается с дочерними объектами `rec`.</span><span class="sxs-lookup"><span data-stu-id="832ce-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="832ce-142">lstDetails заполняется значения из строки `rs`.</span><span class="sxs-lookup"><span data-stu-id="832ce-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="832ce-143">Если ресурс — это простая запись `recFields` вызывается.</span><span class="sxs-lookup"><span data-stu-id="832ce-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="832ce-144">Дополнительные сведения о `recFields`, просмотрите следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="832ce-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="832ce-145">Код не реализуется, если ресурса структурированных документов.</span><span class="sxs-lookup"><span data-stu-id="832ce-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="832ce-146">Шаг 4: Заполните текстовое поле сведений</span><span class="sxs-lookup"><span data-stu-id="832ce-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="832ce-147">Создание нового подпрограммы с именем `recFields` и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="832ce-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   <span data-ttu-id="832ce-148">Этот код заполняет lstDetails с полями и передается значения простой записи `recFields`.</span><span class="sxs-lookup"><span data-stu-id="832ce-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="832ce-149">Если ресурс является текстовым файлом, текст **поток** открывается из записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="832ce-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="832ce-150">Определяет код, если набор знаков ASCII и копирует содержимое **потока** в `txtDetails`.</span><span class="sxs-lookup"><span data-stu-id="832ce-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

