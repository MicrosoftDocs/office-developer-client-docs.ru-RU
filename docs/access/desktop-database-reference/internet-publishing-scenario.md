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
# <a name="internet-publishing-scenario"></a>Сценарий публикации в Интернете

**Область применения**: Access 2013, Office 2013

В этом примере кода показано, как использовать ADO с поставщиком Microsoft OLE DB для публикации в Интернете. В этом сценарии создается приложение Visual Basic, использующее объекты **Recordset,** **Record** и **Stream** для отображения содержимого ресурсов, опубликованных с помощью поставщика интернет-публикации.

Для создания этого сценария необходимо следующее: 

1. Настройка Visual Basic проекта.
2. Инициализация основного списка.
3. Заполнять поле списка "Поля".
4. Заполнять текстовое поле "Сведения".

## <a name="step-1-set-up-the-visual-basic-project"></a>Шаг 1. Настройка Visual Basic проекта

В этом сценарии предполагается, что в вашей системе установлены Microsoft Visual Basic 6.0 или более поздней, ADO 2.5 или более поздней, а также поставщик Microsoft OLE DB для публикации в Интернете.

### <a name="create-an-ado-project"></a>Создание проекта ADO

1.  В Microsoft Visual Basic создайте новый стандартный EXE-проект.

2.  В меню **"Проект"** выберите **ссылки.**

3.  Выберите **библиотеку microsoft ActiveX Data Objects 2.5** и нажмите кнопку **"ОК".**

### <a name="insert-controls-on-the-main-form"></a>Вставка элементов управления в основную форму

1.  Добавление в Form1 управления ListBox. Установите для свойства **Name** свойство **lstMain.**

2.  Добавьте в Form1 еще один контроль ListBox. Установите для **свойства Name** **свойство lstDetails.**

3.  Добавление в Form1 управления TextBox. **Задайте** для свойства Name свойство **txtDetails.**

## <a name="step-2-initialize-the-main-list-box"></a>Шаг 2. Инициализация основного списка

### <a name="declare-global-record-and-recordset-objects"></a>Объявление глобальных объектов Record и Recordset

- Вставьте следующий код в (общие) (объявления) для Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Этот код объявляет глобальные ссылки на объекты **Record** и **Recordset,** которые будут использоваться далее в этом сценарии.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Подключение к URL-адресу и заполнение lstMain

- Вставьте следующий код в обработчик событий загрузки формы для Form1:
    
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
    
   Этот код идирует глобальные объекты **Record** и **Recordset.** Запись **открывается** с URL-адресом, указанным `grec` как **ActiveConnection.** Если URL-адрес существует, он открывается; Если он еще не существует, он создается. 
   
   Обратите внимание, что необходимо `https://servername/foldername/` заменить допустимый URL-адрес из вашей среды. 
   
   Набор **записей** `grs` открывается для его  `grec` детей. Затем lstMain заполняется именами файлов ресурсов, опубликованных по URL-адресу.

## <a name="step-3-populate-the-fields-list-box"></a>Шаг 3. Заполнение списка "Поля"

- Вставьте следующий код в обработок события Click lstMain:

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

   Этот код объявляет и мгновенно регистрирует локальные объекты **Record** и **Recordset** и `rec` `rs` соответственно.

   Строка, соответствующая ресурсу, выбранному в lstMain, является текущей строкой `grs` . Затем **будет** очищено поле со списком сведений, и откроется `rec` текущая строка `grs` источника.

   Если ресурс является записью коллекции (как указано **в RecordType),** локальный набор **записей** открывается на его `rs` `rec` основе. LstDetails затем заполняется значениями из строк `rs` .

   Если ресурс является простой записью, `recFields` он будет вызван. Дополнительные сведения `recFields` см. в следующем шаге.

   Если ресурс является структурированным документом, код не реализуется.

## <a name="step-4-populate-the-details-text-box"></a>Шаг 4. Заполнение текстового окна "Сведения"

- Создайте новую подгруппу с именем `recFields` и вставьте следующий код:

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

   Этот код заполняет lstDetails полями и значениями простой записи, переданной `recFields` в . Если ресурс является текстовым файлом, из записи ресурса открывается текстовый поток.  Код определяет, является ли набор символов ASCII, и копирует содержимое **Stream** в `txtDetails` .

