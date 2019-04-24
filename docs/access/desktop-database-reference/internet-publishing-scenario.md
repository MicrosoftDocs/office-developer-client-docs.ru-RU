---
title: Сценарий публикации в Интернете
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291274"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="20448-102">Сценарий публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="20448-102">Internet publishing scenario</span></span>

<span data-ttu-id="20448-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20448-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20448-104">В этом примере кода показано, как использовать ADO с поставщиком Microsoft OLE DB для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="20448-104">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="20448-105">В этом сценарии вы создадите приложение Visual Basic, которое использует объекты **Recordset**, **Record**и **Stream** для отображения содержимого ресурсов, опубликованных поставщиком публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="20448-105">In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="20448-106">Для создания этого сценария необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="20448-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="20448-107">Настройка проекта Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="20448-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="20448-108">Инициализируйте поле основного списка.</span><span class="sxs-lookup"><span data-stu-id="20448-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="20448-109">ЗаПолните поле списка поля.</span><span class="sxs-lookup"><span data-stu-id="20448-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="20448-110">ЗаПолните текстовое поле сведения.</span><span class="sxs-lookup"><span data-stu-id="20448-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="20448-111">Шаг 1: Настройка проекта Visual Basic</span><span class="sxs-lookup"><span data-stu-id="20448-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="20448-112">В этом сценарии предполагается, что у вас есть Microsoft Visual Basic 6,0 или более поздней версии, ADO 2,5 или более поздней версии, а также поставщик Microsoft OLE DB для публикации в Интернете, установленный в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="20448-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="20448-113">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="20448-113">Create an ADO project</span></span>

1.  <span data-ttu-id="20448-114">В Microsoft Visual Basic создайте стандартный проект EXE.</span><span class="sxs-lookup"><span data-stu-id="20448-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="20448-115">В меню **проект** выберите **ссылки**.</span><span class="sxs-lookup"><span data-stu-id="20448-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="20448-116">Выберите **библиотеку Microsoft ActiveX Data objects 2,5**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="20448-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="20448-117">Вставка элементов управления в главную форму</span><span class="sxs-lookup"><span data-stu-id="20448-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="20448-118">Добавление элемента управления ListBox в форму Form1.</span><span class="sxs-lookup"><span data-stu-id="20448-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="20448-119">ПриСвойте свойству **Name** значение **лстмаин**.</span><span class="sxs-lookup"><span data-stu-id="20448-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="20448-120">Добавьте другой элемент управления ListBox в форму Form1.</span><span class="sxs-lookup"><span data-stu-id="20448-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="20448-121">ПриСвойте свойству **Name** значение **лстдетаилс**.</span><span class="sxs-lookup"><span data-stu-id="20448-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="20448-122">Добавление элемента управления TextBox в форму Form1.</span><span class="sxs-lookup"><span data-stu-id="20448-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="20448-123">ПриСвойте свойству **Name** значение **ткстдетаилс**.</span><span class="sxs-lookup"><span data-stu-id="20448-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="20448-124">Шаг 2: инициализация основного списка</span><span class="sxs-lookup"><span data-stu-id="20448-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="20448-125">Объявление объектов глобальной записи и объектов Recordset</span><span class="sxs-lookup"><span data-stu-id="20448-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="20448-126">Вставьте следующий код в (Общие) (объявления) для Form1:</span><span class="sxs-lookup"><span data-stu-id="20448-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="20448-127">Этот код объявляет ссылки на глобальные объекты для объектов **Record** и **Recordset** , которые будут использоваться позже в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="20448-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="20448-128">Подключение к URL-АДРЕСу и заполнение Лстмаин</span><span class="sxs-lookup"><span data-stu-id="20448-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="20448-129">Вставьте следующий код в обработчик событий загрузки формы для Form1:</span><span class="sxs-lookup"><span data-stu-id="20448-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
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
    
   <span data-ttu-id="20448-130">Этот код создает экземпляр глобальной **записи** и объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="20448-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="20448-131">**Запись** `grec` открывается с URL-адресом, указанным в качестве **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="20448-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="20448-132">Если URL-адрес существует, он будет открыт; Если он еще не существует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="20448-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="20448-133">Обратите внимание, что `https://servername/foldername/` необходимо заменить ДЕЙСТВИТЕЛЬНЫМ URL-адресом в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="20448-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="20448-134">**Набор записей** `grs` открывается для дочерних элементов **записи** `grec`.</span><span class="sxs-lookup"><span data-stu-id="20448-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="20448-135">Затем в Лстмаин заполняются имена файлов ресурсов, опубликованных по URL-АДРЕСу.</span><span class="sxs-lookup"><span data-stu-id="20448-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="20448-136">Шаг 3: заполнение поля списка "поля"</span><span class="sxs-lookup"><span data-stu-id="20448-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="20448-137">Вставьте следующий код в обработчик событий Click объекта Лстмаин:</span><span class="sxs-lookup"><span data-stu-id="20448-137">Insert the following code into the Click event handler of lstMain:</span></span>

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

   <span data-ttu-id="20448-138">Этот код объявляет и создает экземпляры локальных **записей** и объектов \*\*\*\* `rec` Recordset и `rs`соответственно.</span><span class="sxs-lookup"><span data-stu-id="20448-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="20448-139">Строка, соответствующая ресурсу, выбранному в Лстмаин, становится текущей строкой `grs`.</span><span class="sxs-lookup"><span data-stu-id="20448-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="20448-140">После этого список " **сведения** " очищается `rec` и открывается с текущей строкой в `grs` качестве источника.</span><span class="sxs-lookup"><span data-stu-id="20448-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="20448-141">Если ресурс является записью коллекции (как указано в **RecordType**), то локальный **набор записей** `rs` открывается на дочерних элементах `rec`.</span><span class="sxs-lookup"><span data-stu-id="20448-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="20448-142">затем Лстдетаилс заполняется значениями из строк `rs`.</span><span class="sxs-lookup"><span data-stu-id="20448-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="20448-143">Если ресурс является простой записью, `recFields` вызывается.</span><span class="sxs-lookup"><span data-stu-id="20448-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="20448-144">Для получения дополнительных сведений `recFields`обратитесь к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="20448-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="20448-145">Если ресурс является структурированным документом, код не реализуется.</span><span class="sxs-lookup"><span data-stu-id="20448-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="20448-146">Шаг 4: заполнение текстового поля сведений</span><span class="sxs-lookup"><span data-stu-id="20448-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="20448-147">Создайте новую подпрограмму с `recFields` именем и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="20448-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

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

   <span data-ttu-id="20448-148">Этот код заполняет Лстдетаилс полями и значениями простой записи, переданной в элемент `recFields`.</span><span class="sxs-lookup"><span data-stu-id="20448-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="20448-149">Если ресурс является текстовым файлом, в записи ресурса открывается текстовый **поток** .</span><span class="sxs-lookup"><span data-stu-id="20448-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="20448-150">Код определяет, является ли набор знаков ASCII, и копирует содержимое **потока** в `txtDetails`.</span><span class="sxs-lookup"><span data-stu-id="20448-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

