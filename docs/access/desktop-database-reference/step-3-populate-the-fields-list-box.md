---
title: 'Шаг 3: Заполнения списка полей'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca764e2339d0c866922be2982a168afc03d84c1d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480430"
---
# <a name="step-3-populate-the-fields-list-box"></a>Шаг 3: Заполнения списка полей


**Применимо к**: Access 2013 | Office 2013

## <a name="step-3-populate-the-fields-list-box"></a>Шаг 3: Заполнения списка полей

**Для заполнения списка полей**

Вставьте следующий код в обработчик событий Click lstMain:

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

Этот код объявляет и создает экземпляр локальной **записи** и объектов **наборов записей** , записи и и rs, соответственно.

Строка, соответствующий ресурсов, выбранных в lstMain становится текущей строки grs. Затем **сведения о** списке флажка и открывается записей с текущей строки. Затем **сведения о** списке флажка и открывается с текущей строки grs в качестве источника записей.

Если ресурс является записью семейства сайтов (в соответствии с **типом записи**), локального **набора записей**, rs, открывается на дочерних записей. Затем lstDetails заполняется значениями из строки открывается на дочерних записей. Затем lstDetails заполняется значениями из строки rs.

Если простой записи ресурса, называется recFields. Дополнительные сведения о recFields можно следующим шагом.

Код не реализуется, если ресурса структурированных документов.

