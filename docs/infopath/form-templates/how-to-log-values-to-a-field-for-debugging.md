---
title: Значения журнала на поле для отладки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: При отладке шаблона формы InfoPath часто полезно заносить значения непосредственно в поле формы для создания записи данных отладки в ходе сеанса тестирования формы. В следующих процедурах описывается создание многострочного поля с последующим добавлением в код формы вспомогательных функций, которые позволяют заносить данные отладки в это поле.
ms.openlocfilehash: f763e6b5d14fe5a5b4d9218af4acd0bc05a242af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807506"
---
# <a name="log-values-to-a-field-for-debugging"></a>Значения журнала на поле для отладки

При отладке шаблона формы InfoPath часто полезно заносить значения непосредственно в поле формы для создания записи данных отладки в ходе сеанса тестирования формы. В следующих процедурах описывается создание многострочного поля с последующим добавлением в код формы вспомогательных функций, которые позволяют заносить данные отладки в это поле.
  
## <a name="create-a-multi-line-text-field"></a>Создание многострочного текстового поля

1. Добавьте в форму элемент управления **Текстовое поле** и измените его размер таким образом, чтобы он поддерживал отображение нескольких строк. 
    
2. Щелкните этот элемент управления правой кнопкой мыши, выберите пункт **Свойства текстового поля**, а затем установите флажок **Многострочное** на вкладке **Отображение**. 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Добавление вспомогательные функции для записи в журнал отладочные данные в поле

1. На вкладке **Разработчик** щелкните элемент **Редактор кода** и сохраните шаблон формы при появлении соответствующего запроса.
    
2. В редакторе кода добавьте следующие три вспомогательные функции в открытый класс в файле кода формы.
    
   > [!IMPORTANT]
   > [!Важно!] Убедитесь, что значение переменной  `debugFieldXpath` в функции  `AddToDebugField` обновлено с использованием правильного выражения XPath для поля, связанного с созданным в рамках первой процедуры элементом управления. 
  
    ```cs
        private void AddToDebugField(string valueToAdd)
        {
            // Update the value of debugFieldXpath to the XPath of the
            // multi-line field where you want to log debug information.
            string debugFieldXpath = "/my:myFields/my:field1";
            string headerLine = "----------------- " + DateTime.Now + 
                " -----------------" + "\r\n";
            SetDebugFieldValue(debugFieldXpath, headerLine + valueToAdd + 
                "\r\n" + GetDebugFieldValue(debugFieldXpath));
        }
        private string GetDebugFieldValue(string xpath)
        {
            return this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).Value;
        }
        private void SetDebugFieldValue(string xpath, string value)
        {
            this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).SetValue(value);
        }
    ```

    ```vb
        Private Sub AddToDebugField(ByVal valueToAdd As String)
            ' Update the value of debugFieldXpath to the XPath of the 
            ' multi-line field where you want to log debug information.
            Dim debugFieldXpath As String = "/my:myFields/my:field1"
            Dim headerLine As String = "----------------- " _
                &amp; DateTime.Now &amp; " -----------------" &amp; vbCrLf
            SetDebugFieldValue(debugFieldXpath, (headerLine &amp; valueToAdd &amp; vbCrLf) _
                &amp; GetDebugFieldValue(debugFieldXpath))
        End Sub
        Private Function GetDebugFieldValue(ByVal xpath As String) As String
            Return Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).Value
        End Function
        Private Sub SetDebugFieldValue(ByVal xpath As String, ByVal value As String)
            Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).SetValue(value)
        End Sub
    ```

> [!NOTE] 
> Если используется Visual Basic, добавьте `Imports Microsoft.VisualBasic.Constants` директив в верхней части файла кода формы. 
  
## <a name="test-the-addtodebugfield-function"></a>Проверка функции AddToDebugField

1. На вкладке **Разработчик** выберите элемент **Событие "Загрузка"** и добавьте следующую строку кода в обработчик события.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. На вкладке **Разработчик** выберите элемент **Событие ""Представление изменено"** и добавьте следующую строку кода в обработчик события.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. На вкладке **Главная** выберите команду **Просмотр**.
    
   В этом поле отладки должны отображаться две записи. Первая запись свидетельствует о загрузке формы, а вторая определяет имя представления. В этих примерах используются обработчики событий, возникающих при открытии формы. При необходимости можно вызывать функцию  `AddToDebugField` после загрузки формы из других обработчиков событий в дополнение к другому коду, выполняемому в контексте формы. 
  

