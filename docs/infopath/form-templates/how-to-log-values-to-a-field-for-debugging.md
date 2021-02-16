---
title: Запись значений в поле для отладки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: При отладке шаблона формы InfoPath часто полезно заносить значения непосредственно в поле формы для создания записи данных отладки в ходе сеанса тестирования формы. В следующих процедурах описывается создание многострочного поля с последующим добавлением в код формы вспомогательных функций, которые позволяют заносить данные отладки в это поле.
ms.openlocfilehash: 28f2a1ad3c13aefd9f898bdf397c9103df98d3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431815"
---
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="d2527-104">Запись значений в поле для отладки</span><span class="sxs-lookup"><span data-stu-id="d2527-104">Log values to a field for debugging</span></span>

<span data-ttu-id="d2527-p102">При отладке шаблона формы InfoPath часто полезно заносить значения непосредственно в поле формы для создания записи данных отладки в ходе сеанса тестирования формы. В следующих процедурах описывается создание многострочного поля с последующим добавлением в код формы вспомогательных функций, которые позволяют заносить данные отладки в это поле.</span><span class="sxs-lookup"><span data-stu-id="d2527-p102">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="d2527-107">Создание многостроального текстового поля</span><span class="sxs-lookup"><span data-stu-id="d2527-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="d2527-108">Добавьте в форму элемент управления **Текстовое поле** и измените его размер таким образом, чтобы он поддерживал отображение нескольких строк.</span><span class="sxs-lookup"><span data-stu-id="d2527-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="d2527-109">Щелкните этот элемент управления правой кнопкой мыши, выберите пункт **Свойства текстового поля**, а затем установите флажок **Многострочное** на вкладке **Отображение**.</span><span class="sxs-lookup"><span data-stu-id="d2527-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="d2527-110">Добавление в поле дополнительных функций для регистрации данных отлаки</span><span class="sxs-lookup"><span data-stu-id="d2527-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="d2527-111">На вкладке **Разработчик** щелкните элемент **Редактор кода** и сохраните шаблон формы при появлении соответствующего запроса.</span><span class="sxs-lookup"><span data-stu-id="d2527-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="d2527-112">В редакторе кода добавьте следующие три вспомогательные функции в открытый класс в файле кода формы.</span><span class="sxs-lookup"><span data-stu-id="d2527-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="d2527-113">[!Важно!] Убедитесь, что значение переменной  `debugFieldXpath` в функции  `AddToDebugField` обновлено с использованием правильного выражения XPath для поля, связанного с созданным в рамках первой процедуры элементом управления.</span><span class="sxs-lookup"><span data-stu-id="d2527-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="d2527-114">При использовании Visual Basic добавьте  `Imports Microsoft.VisualBasic.Constants` директивы в верхней части файла кода формы.</span><span class="sxs-lookup"><span data-stu-id="d2527-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="d2527-115">Проверка функции AddToDebugField</span><span class="sxs-lookup"><span data-stu-id="d2527-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="d2527-116">На вкладке **Разработчик** выберите элемент **Событие "Загрузка"** и добавьте следующую строку кода в обработчик события.</span><span class="sxs-lookup"><span data-stu-id="d2527-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="d2527-117">На вкладке **Разработчик** выберите элемент **Событие ""Представление изменено"** и добавьте следующую строку кода в обработчик события.</span><span class="sxs-lookup"><span data-stu-id="d2527-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="d2527-118">На вкладке **Главная** выберите команду **Просмотр**.</span><span class="sxs-lookup"><span data-stu-id="d2527-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="d2527-p103">В этом поле отладки должны отображаться две записи. Первая запись свидетельствует о загрузке формы, а вторая определяет имя представления. В этих примерах используются обработчики событий, возникающих при открытии формы. При необходимости можно вызывать функцию  `AddToDebugField` после загрузки формы из других обработчиков событий в дополнение к другому коду, выполняемому в контексте формы.</span><span class="sxs-lookup"><span data-stu-id="d2527-p103">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view. These examples use event handlers for events that occur as the form is opened. However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  

