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

В этом примере кода показано, как использовать ADO с поставщиком Microsoft OLE DB для публикации в Интернете. В этом сценарии вы создадите приложение Visual Basic, которое использует объекты **Recordset**, **Record**и **Stream** для отображения содержимого ресурсов, опубликованных поставщиком публикации в Интернете.

Для создания этого сценария необходимо выполнить следующие действия: 

1. Настройка проекта Visual Basic.
2. Инициализируйте поле основного списка.
3. Заполните поле списка поля.
4. Заполните текстовое поле сведения.

## <a name="step-1-set-up-the-visual-basic-project"></a>Шаг 1: Настройка проекта Visual Basic

В этом сценарии предполагается, что у вас есть Microsoft Visual Basic 6,0 или более поздней версии, ADO 2,5 или более поздней версии, а также поставщик Microsoft OLE DB для публикации в Интернете, установленный в вашей системе.

### <a name="create-an-ado-project"></a>Создание проекта ADO

1.  В Microsoft Visual Basic создайте стандартный проект EXE.

2.  В меню **проект** выберите **ссылки**.

3.  Выберите **библиотеку Microsoft ActiveX Data objects 2,5**и нажмите кнопку **ОК**.

### <a name="insert-controls-on-the-main-form"></a>Вставка элементов управления в главную форму

1.  Добавление элемента управления ListBox в форму Form1. Присвойте свойству **Name** значение **лстмаин**.

2.  Добавьте другой элемент управления ListBox в форму Form1. Присвойте свойству **Name** значение **лстдетаилс**.

3.  Добавление элемента управления TextBox в форму Form1. Присвойте свойству **Name** значение **ткстдетаилс**.

## <a name="step-2-initialize-the-main-list-box"></a>Шаг 2: инициализация основного списка

### <a name="declare-global-record-and-recordset-objects"></a>Объявление объектов глобальной записи и объектов Recordset

- Вставьте следующий код в (Общие) (объявления) для Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Этот код объявляет ссылки на глобальные объекты для объектов **Record** и **Recordset** , которые будут использоваться позже в этом сценарии.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Подключение к URL-адресу и заполнение Лстмаин

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
    
   Этот код создает экземпляр глобальной **записи** и объектов **Recordset** . **Запись** `grec` открывается с URL-адресом, указанным в качестве **ActiveConnection**. Если URL-адрес существует, он будет открыт; Если он еще не существует, он будет создан. 
   
   Обратите внимание, что `https://servername/foldername/` необходимо заменить действительным URL-адресом в вашей среде. 
   
   **Набор записей** `grs` открывается для дочерних элементов **записи** `grec`. Затем в Лстмаин заполняются имена файлов ресурсов, опубликованных по URL-адресу.

## <a name="step-3-populate-the-fields-list-box"></a>Шаг 3: заполнение поля списка "поля"

- Вставьте следующий код в обработчик событий Click объекта Лстмаин:

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

   Этот код объявляет и создает экземпляры локальных **записей** и объектов **Recordset** `rec` Recordset и `rs`соответственно.

   Строка, соответствующая ресурсу, выбранному в Лстмаин, становится текущей строкой `grs`. После этого список " **сведения** " очищается `rec` и открывается с текущей строкой в `grs` качестве источника.

   Если ресурс является записью коллекции (как указано в **RecordType**), то локальный **набор записей** `rs` открывается на дочерних элементах `rec`. затем Лстдетаилс заполняется значениями из строк `rs`.

   Если ресурс является простой записью, `recFields` вызывается. Для получения дополнительных сведений `recFields`обратитесь к следующему шагу.

   Если ресурс является структурированным документом, код не реализуется.

## <a name="step-4-populate-the-details-text-box"></a>Шаг 4: заполнение текстового поля сведений

- Создайте новую подпрограмму с `recFields` именем и вставьте следующий код:

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

   Этот код заполняет Лстдетаилс полями и значениями простой записи, переданной в элемент `recFields`. Если ресурс является текстовым файлом, в записи ресурса открывается текстовый **поток** . Код определяет, является ли набор знаков ASCII, и копирует содержимое **потока** в `txtDetails`.

