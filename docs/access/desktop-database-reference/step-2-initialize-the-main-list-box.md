---
title: Этап 2. Инициализация главного списка
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3505c2726da3f2f2f01d179c97cde5a1d7b635ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869899"
---
# <a name="step-2-initialize-the-main-list-box"></a>Этап 2. Инициализация главного списка


**Применимо к**: Access 2013, Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Этап 2. Инициализация главного списка

**Объявите глобальные объекты набора записей и записи**

  - Вставьте следующий код в (Общие) (раздел описаний) для Form1:
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    Этот код объявляет ссылки на глобальный объект для объектов **записи** и **записей** , которые будут использоваться позже в этом сценарии.

**Чтобы подключиться к URL-адрес и заполнения lstMain**

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
    
    Этот код создает глобальные объекты **набора записей** и **записи** . **Запись**, grec, открывается с URL-адрес, указанный в качестве **ActiveConnection**. Если существует URL-адрес, он открывается; Если он еще не существует, он будет создан. Обратите внимание, что необходимо заменить "https://servername/foldername/" с допустимый URL-адрес из среды. **Набор записей**, grs, открывается на дочерних элементов в **запись**grec. Затем lstMain содержит имена файлов ресурсов, опубликованные в URL-адрес.

