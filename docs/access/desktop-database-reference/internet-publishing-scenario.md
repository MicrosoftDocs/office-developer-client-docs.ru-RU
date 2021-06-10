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
# <a name="internet-publishing-scenario"></a><span data-ttu-id="7dfd7-102">Сценарий публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="7dfd7-102">Internet publishing scenario</span></span>

<span data-ttu-id="7dfd7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dfd7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dfd7-104">В этом примере кода показано, как использовать ADO с поставщиком DB Microsoft OLE для публикации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-104">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="7dfd7-105">В этом сценарии будет Visual Basic приложение, использующее объекты **Recordset,** **Record** и **Stream** для отображения содержимого ресурсов, опубликованных с помощью поставщика публикаций в Интернете.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-105">In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="7dfd7-106">Для создания этого сценария необходимы следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7dfd7-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="7dfd7-107">Настройка проекта Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="7dfd7-108">Инициализация основного списка.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="7dfd7-109">Заполнять поле списка Поля.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="7dfd7-110">Заполнять текстовое поле Details.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="7dfd7-111">Шаг 1. Настройка Visual Basic проекта</span><span class="sxs-lookup"><span data-stu-id="7dfd7-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="7dfd7-112">В этом сценарии предполагается, что в Visual Basic microsoft Visual Basic 6.0 или более поздней, ADO 2.5 или более поздней, а также установлен поставщик microsoft OLE DB для интернет-публикации в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="7dfd7-113">Создание проекта ADO</span><span class="sxs-lookup"><span data-stu-id="7dfd7-113">Create an ADO project</span></span>

1.  <span data-ttu-id="7dfd7-114">В microsoft Visual Basic создайте новый проект Standard EXE.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="7dfd7-115">Из меню **Project** выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="7dfd7-116">Выберите **библиотеку ActiveX объектов данных Microsoft 2.5 и** нажмите **кнопку ОК.**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="7dfd7-117">Вставка элементов управления в основную форму</span><span class="sxs-lookup"><span data-stu-id="7dfd7-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="7dfd7-118">Добавьте в Form1 управление ListBox.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="7dfd7-119">Установите свойство **Name** **для lstMain.**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="7dfd7-120">Добавьте еще один контроль ListBox в Form1.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="7dfd7-121">Установите свойство **Name** **для lstDetails.**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="7dfd7-122">Добавьте управление TextBox в Form1.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="7dfd7-123">Установите свойство **Name** **txtDetails.**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="7dfd7-124">Шаг 2. Инициализация основного окна списка</span><span class="sxs-lookup"><span data-stu-id="7dfd7-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="7dfd7-125">Объявление объектов глобальной записи и recordset</span><span class="sxs-lookup"><span data-stu-id="7dfd7-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="7dfd7-126">Вставьте следующий код в (Общие) (Объявления) для Form1:</span><span class="sxs-lookup"><span data-stu-id="7dfd7-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="7dfd7-127">Этот код объявляет глобальные ссылки на **объекты Record** и **Recordset,** которые будут использоваться позже в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="7dfd7-128">Подключение URL-адрес и заполнять lstMain</span><span class="sxs-lookup"><span data-stu-id="7dfd7-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="7dfd7-129">Вставьте следующий код в обработчик событий загрузки форм для Form1:</span><span class="sxs-lookup"><span data-stu-id="7dfd7-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
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
    
   <span data-ttu-id="7dfd7-130">Этот код мгновенно привносят глобальные **объекты Record** и **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="7dfd7-131">Запись **открывается** `grec` URL-адресом, указанным как **ActiveConnection.**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="7dfd7-132">Если URL-адрес существует, он открывается; если она еще не существует, она создается.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="7dfd7-133">Обратите внимание, что необходимо `https://servername/foldername/` заменить допустимый URL-адрес из среды.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="7dfd7-134">Набор **записей** `grs` открыт для детей **записи.** `grec`</span><span class="sxs-lookup"><span data-stu-id="7dfd7-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="7dfd7-135">Затем lstMain заполняется именами файлов ресурсов, опубликованных на URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="7dfd7-136">Шаг 3. Заполнять поле списка Поля</span><span class="sxs-lookup"><span data-stu-id="7dfd7-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="7dfd7-137">Вставьте следующий код в обработник событий Click lstMain:</span><span class="sxs-lookup"><span data-stu-id="7dfd7-137">Insert the following code into the Click event handler of lstMain:</span></span>

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

   <span data-ttu-id="7dfd7-138">Этот код объявляет и мгновенно передает локальные объекты **Record** и **Recordset** и `rec` `rs` соответственно.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="7dfd7-139">Строка, соответствующая ресурсу, выбранному в lstMain, выполнена в текущей строке `grs` .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="7dfd7-140">Затем **поле Список** сведений очищается и открывается с текущей `rec` строкой в качестве `grs` источника.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="7dfd7-141">Если ресурс является записью коллекции (как указано **в RecordType),** локальный набор записей открывается для  `rs` детей `rec` .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="7dfd7-142">затем lstDetails заполняется значениями из строк `rs` .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="7dfd7-143">Если ресурс является простой записью, `recFields` называется.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="7dfd7-144">Дополнительные сведения `recFields` см. в следующем шаге.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="7dfd7-145">Если ресурс является структурированным документом, код не реализуется.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="7dfd7-146">Шаг 4. Заполнение текстового окна Details</span><span class="sxs-lookup"><span data-stu-id="7dfd7-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="7dfd7-147">Создайте новый подраутин с именем `recFields` и вставьте следующий код:</span><span class="sxs-lookup"><span data-stu-id="7dfd7-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

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

   <span data-ttu-id="7dfd7-148">Этот код заполняет lstDetails полями и значениями простой записи, переданной `recFields` в .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="7dfd7-149">Если ресурс — это текстовый файл, текстовый **поток** открывается из записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="7dfd7-150">Код определяет, является ли набор символов ASCII, и копирует содержимое **Stream** в `txtDetails` .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

