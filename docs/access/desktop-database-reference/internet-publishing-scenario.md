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

В этом примере кода показано, как использовать ADO с поставщиком DB Microsoft OLE для публикации в Интернете. В этом сценарии будет Visual Basic приложение, использующее объекты **Recordset,** **Record** и **Stream** для отображения содержимого ресурсов, опубликованных с помощью поставщика публикаций в Интернете.

Для создания этого сценария необходимы следующие действия: 

1. Настройка проекта Visual Basic.
2. Инициализация основного списка.
3. Заполнять поле списка Поля.
4. Заполнять текстовое поле Details.

## <a name="step-1-set-up-the-visual-basic-project"></a>Шаг 1. Настройка Visual Basic проекта

В этом сценарии предполагается, что в Visual Basic microsoft Visual Basic 6.0 или более поздней, ADO 2.5 или более поздней, а также установлен поставщик microsoft OLE DB для интернет-публикации в вашей системе.

### <a name="create-an-ado-project"></a>Создание проекта ADO

1.  В microsoft Visual Basic создайте новый проект Standard EXE.

2.  Из меню **Project** выберите **Ссылки**.

3.  Выберите **библиотеку ActiveX объектов данных Microsoft 2.5 и** нажмите **кнопку ОК.**

### <a name="insert-controls-on-the-main-form"></a>Вставка элементов управления в основную форму

1.  Добавьте в Form1 управление ListBox. Установите свойство **Name** **для lstMain.**

2.  Добавьте еще один контроль ListBox в Form1. Установите свойство **Name** **для lstDetails.**

3.  Добавьте управление TextBox в Form1. Установите свойство **Name** **txtDetails.**

## <a name="step-2-initialize-the-main-list-box"></a>Шаг 2. Инициализация основного окна списка

### <a name="declare-global-record-and-recordset-objects"></a>Объявление объектов глобальной записи и recordset

- Вставьте следующий код в (Общие) (Объявления) для Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Этот код объявляет глобальные ссылки на **объекты Record** и **Recordset,** которые будут использоваться позже в этом сценарии.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Подключение URL-адрес и заполнять lstMain

- Вставьте следующий код в обработчик событий загрузки форм для Form1:
    
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
    
   Этот код мгновенно привносят глобальные **объекты Record** и **Recordset.** Запись **открывается** `grec` URL-адресом, указанным как **ActiveConnection.** Если URL-адрес существует, он открывается; если она еще не существует, она создается. 
   
   Обратите внимание, что необходимо `https://servername/foldername/` заменить допустимый URL-адрес из среды. 
   
   Набор **записей** `grs` открыт для детей **записи.** `grec` Затем lstMain заполняется именами файлов ресурсов, опубликованных на URL-адрес.

## <a name="step-3-populate-the-fields-list-box"></a>Шаг 3. Заполнять поле списка Поля

- Вставьте следующий код в обработник событий Click lstMain:

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

   Этот код объявляет и мгновенно передает локальные объекты **Record** и **Recordset** и `rec` `rs` соответственно.

   Строка, соответствующая ресурсу, выбранному в lstMain, выполнена в текущей строке `grs` . Затем **поле Список** сведений очищается и открывается с текущей `rec` строкой в качестве `grs` источника.

   Если ресурс является записью коллекции (как указано **в RecordType),** локальный набор записей открывается для  `rs` детей `rec` . затем lstDetails заполняется значениями из строк `rs` .

   Если ресурс является простой записью, `recFields` называется. Дополнительные сведения `recFields` см. в следующем шаге.

   Если ресурс является структурированным документом, код не реализуется.

## <a name="step-4-populate-the-details-text-box"></a>Шаг 4. Заполнение текстового окна Details

- Создайте новый подраутин с именем `recFields` и вставьте следующий код:

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

   Этот код заполняет lstDetails полями и значениями простой записи, переданной `recFields` в . Если ресурс — это текстовый файл, текстовый **поток** открывается из записи ресурса. Код определяет, является ли набор символов ASCII, и копирует содержимое **Stream** в `txtDetails` .

