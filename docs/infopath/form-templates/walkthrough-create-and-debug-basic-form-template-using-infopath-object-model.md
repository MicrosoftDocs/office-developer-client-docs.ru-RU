---
title: 'Walkthrough: Create and debug a basic form template using the InfoPath object model'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- шаблоны форм [infopath 2007], по walkthroughs,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: В этом разделе приводится по walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the Microsoft.Office.Interop.InfoPath.SemiTrust namespace.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414342"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Walkthrough: Create and debug a basic form template using the InfoPath object model

В этом разделе приводится по walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace. 
  
## <a name="hello-world"></a>Hello World

В следующем примере вы узнаете, как отобразить простое диалоговое окно оповещения с помощью метода [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) объектной модели, совместимой с InfoPath 2003. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Создание нового шаблона формы InfoPath, работающего с объектной моделью, совместимой с InfoPath 2003

1. Создайте новый шаблон формы, который работает с объектной моделью, совместимой с InfoPath 2003, как описано в описании создания шаблона формы с помощью объектной модели [InfoPath 2003.](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)
    
2. Введите имя проекта шаблона формы HelloWorld и сохраните проект. 
    
   Проектная система создаст файлы кода и проекта, а затем откроет пустой шаблон формы в режиме конструктора InfoPath. Теперь можно добавлять обработчики событий.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Добавление кнопки с обработчиком событий OnClick

1. В разделе **Элементы управления** вкладки **Главная** щелкните элемент управления **Кнопка**, чтобы вставить его в представление. 
    
2. Щелкните правой кнопкой мыши элемент управления и выберите **Свойства кнопки**.
    
3. Измените **метку на** "Оповещение".
    
4. Измените **ID на** AlertID.
    
5. Щелкните **Редактировать код формы**.
    
   Создается обработка события [OnClick,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) и фокус перемещается на редактор кода в Visual Studio 2012. Дополнительные сведения о работе с обработчиками событий см. в подразделе "Добавление обработчиков событий с помощью объектной модели [InfoPath 2003".](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md) 
    
   Теперь можно добавить код формы для обработчика событий кнопки.
    
### <a name="add-form-code-to-the-event-handler"></a>Добавление кода формы для обработчика событий

1. Введите в обработчике событий **OnClick** следующий код: 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Обратите внимание, что после ввода каждой точки в строке кода отображается раскрывающийся список Microsoft IntelliSense. Целиком обработчик событий должен выглядеть следующим образом:
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > В качестве альтернативы использованию метода **Alert** можно воспользоваться методом **MessageBox.Show** пространства имен **System.Windows.Forms** для отображения окна сообщения. Для этого необходимо добавить ссылку на сборку System.Windows.Forms, добавить директивы или к директивам в начале файла `using System.Windows.Forms;` кода, а затем ввести строку кода, например: `Imports System.Windows.Forms``MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Переключитесь в окно режима конструктора InfoPath и нажмите кнопку **Просмотр** на вкладке **Главная**. 
    
3. В окне **Просмотр** нажмите кнопку **Оповещение**. 
    
   Отобразится окно с текстовым сообщением "Hello World!"
    
   В следующей процедуре показано, как добавить отладочные точки останова в код формы.
    
### <a name="debug-form-code"></a>Отладка кода формы

1. В редакторе кода щелкните серую полоску слева от строки:
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Отобразится красный кружок, а строка кода будет выделена, указывая, что при запуске кода формы возникнет пауза в этой точке останова.
    
2. В меню **Отладка** выберите пункт **Начать отладку** (или нажмите клавишу F5). 
    
3. В окне InfoPath **Просмотр** нажмите кнопку **Оповещение**. 
    
   Фокус перемещается на редактор кода, и выделяется строка точки останова.
    
4. В меню **Отладка** выберите пункт **Шаг с обходом** (или нажмите сочетание клавиш SHIFT+F8), чтобы продолжить обход кода. 
    
   Выполняется **код** метода Alert и "Hello World!" оповещение отображается в окне InfoPath **Preview.** 
    
## <a name="getting-the-current-users-name"></a>Получение имени текущего пользователя

С помощью классов .NET Framework можно получить доступ к возможностям, которые сложно реализовать в скрипте. В этом примере предоставляется обучение использованию классов .NET Framework для получения имени текущего пользователя.
  
### <a name="add-an-onload-event-handler"></a>Добавление обработчика событий OnLoad

1. Откройте проект InfoPath "HelloWorld", созданный ранее.
    
2. На вкладке **Вид** выберите пункт **Отобразить поля**.
    
3. Щелкните правой кнопкой мыши узел **myFields**, а затем щелкните **Добавить**.
    
4. В поле **Имя** введите **employee** и нажмите кнопку **ОК**.
    
5. Перетащите узел **employee** в представление. 
    
6. На вкладке **Разработчик** щелкните **Событие OnLoad**.
    
   При этом будет создаваться обработок события [OnLoad,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) а фокус перемещается на редактор кода. Код этого обработчика событий будет вызываться при каждой загрузке формы. В следующей процедуре демонстрируется добавление кода формы, получающего имя пользователя для обработчика событий. 
    
### <a name="add-form-code"></a>Добавление кода формы 

1. Введите в обработчике событий **OnLoad** следующий код: 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. Скомпилируйте и просмотрите форму.
    
   Теперь в текстовом поле employee должно быть выведено текущее имя пользователя. 
    
Сведения о развертывании шаблона формы с управляемым кодом см. в под названием "Развертывание шаблонов форм [InfoPath с кодом".](how-to-deploy-infopath-form-templates-with-code.md) Сведения об объектной модели InfoPath и распространенных задачах программирования в шаблонах форм с управляемым кодом, которые работают с объектной моделью, совместимой с InfoPath 2003, см. в подразделе "Общие сведения об объектной модели [InfoPath 2003".](understanding-the-infopath-2003-object-model.md) 
  
## <a name="see-also"></a>См. также

- [Инициализация и очистка кода с помощью объектной модели InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [Объектные модели, совместимые с InfoPath 2003](infopath-2003-compatible-object-models.md)
- [Добавление обработера событий с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

