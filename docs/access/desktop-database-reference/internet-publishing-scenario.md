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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708510"
---
# <a name="internet-publishing-scenario"></a>Сценарий публикации в Интернете

**Применимо к**: Access 2013, Office 2013

В этом примере кода показано, как использовать ADO с поставщик Microsoft OLE DB для публикации Интернет. В данном сценарии создается приложения Visual Basic, использующего объекты **набора записей**, **записи**и **поток** для отображения содержимого из ресурсов, опубликованные с поставщиком публикации Интернет.

Для создания этого сценария необходимы следующие действия: 

1. Настройка проекта Visual Basic.
2. Инициализируйте поле со списком Main.
3. Заполните поля.
4. Заполните текстовое поле сведений.

## <a name="step-1-set-up-the-visual-basic-project"></a>Этап 1: Настройка проекта Visual Basic

В этом сценарии предполагается, что у вас есть Microsoft Visual Basic 6.0 или более поздней версии, ADO 2.5 или более поздней версии и поставщик Microsoft OLE DB для публикации Интернет в системе.

### <a name="create-an-ado-project"></a>Создание проекта ADO

1.  В Microsoft Visual Basic, создайте новый проект стандартный exe-ФАЙЛ.

2.  В меню **проект** выберите команду **Справочные материалы**.

3.  Выберите **Библиотеку 2.5 объекты данных ActiveX Microsoft**и нажмите кнопку **ОК**.

### <a name="insert-controls-on-the-main-form"></a>Вставка элементов управления в форме

1.  Добавьте в форму Form1 элемент управления ListBox. Установите для свойства **имя** **lstMain**.

2.  Добавьте другой элемент управления ListBox Form1. Установите для свойства **имя** **lstDetails**.

3.  Добавьте элемент управления TextBox в форму Form1. Установите для свойства **имя** **txtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Шаг 2: Инициализировать поле со списком Main

### <a name="declare-global-record-and-recordset-objects"></a>Объявите глобальные объекты набора записей и записи

- Вставьте следующий код в (Общие) (раздел описаний) для Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Этот код объявляет ссылки на глобальный объект для объектов **записи** и **записей** , которые будут использоваться позже в этом сценарии.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Подключение к URL-адрес и заполнения lstMain

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
    
   Этот код создает глобальные объекты **набора записей** и **записи** . **Запись** `grec` открывается с URL-адрес, указанный в качестве **ActiveConnection**. Если существует URL-адрес, он открывается; Если он еще не существует, он будет создан. 
   
   Обратите внимание, что необходимо заменить `https://servername/foldername/` с допустимый URL-адрес из среды. 
   
   **Набор записей** `grs` открывается на дочерних элементов **записи** `grec`. Затем lstMain заполняется имена файлов ресурсов, опубликованные в URL-адрес.

## <a name="step-3-populate-the-fields-list-box"></a>Шаг 3: Заполнения списка полей

- Вставьте следующий код в обработчик событий Click lstMain:

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

   Этот код объявляет и создает локальные объекты **набора записей** и **записи** `rec` и `rs`соответственно.

   Строку, соответствующую ресурсов, выбранных в lstMain будет создано текущей строки `grs`. **Сведения о** списке затем флажка и `rec` открывается с текущей строки `grs` как источник.

   Если ресурс коллекцию записи (в соответствии с **типом записи**), локального **набора записей** `rs` открывается с дочерними объектами `rec`. lstDetails заполняется значения из строки `rs`.

   Если ресурс — это простая запись `recFields` вызывается. Дополнительные сведения о `recFields`, просмотрите следующий шаг.

   Код не реализуется, если ресурса структурированных документов.

## <a name="step-4-populate-the-details-text-box"></a>Шаг 4: Заполните текстовое поле сведений

- Создание нового подпрограммы с именем `recFields` и вставьте следующий код:

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

   Этот код заполняет lstDetails с полями и передается значения простой записи `recFields`. Если ресурс является текстовым файлом, текст **поток** открывается из записи ресурса. Определяет код, если набор знаков ASCII и копирует содержимое **потока** в `txtDetails`.

