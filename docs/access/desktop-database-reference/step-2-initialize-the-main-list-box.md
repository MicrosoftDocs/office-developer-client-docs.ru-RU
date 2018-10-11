---
title: 'Шаг 2: Инициализация главном списке'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482193"
---
# <a name="step-2-initialize-the-main-list-box"></a>Шаг 2: Инициализация главном списке


**Применимо к**: Access 2013 | Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Шаг 2: Инициализация главном списке

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

