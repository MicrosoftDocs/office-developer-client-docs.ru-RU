---
title: 'Пошаговое руководство: Создание и отладка шаблона базовой формы с помощью объектной модели InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- шаблоны [InfoPath 2007], создание совместимых с InfoPath 2003, совместимых с InfoPath 2003 шаблонов форм, пошаговые руководства по форм шаблонов форм [infopath 2007], примеры,
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Этот раздел представляет собой пошаговое руководство по созданию базового шаблона форм управляемого кода InfoPath, работающего с объектной моделью совместимых с InfoPath 2003, предоставляемой пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: 3939cfcfdf2a8683fe614c5f49cc8b2719484ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807596"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Пошаговое руководство: Создание и отладка шаблона базовой формы с помощью объектной модели InfoPath

Этот раздел представляет собой пошаговое руководство по созданию базового шаблона форм управляемого кода InfoPath, работающего с объектной моделью совместимых с InfoPath 2003, предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="hello-world"></a>Hello World

В следующем примере вы узнаете, как для отображения простого диалогового окна оповещения с помощью метода [оповещение](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) объектной модели, совместимой с InfoPath 2003. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Создание нового шаблона формы InfoPath, работающего с объектной моделью, совместимой с InfoPath 2003

1. Создание нового шаблона формы, который работает с помощью объектной модели, совместимой с InfoPath 2003, как описано в разделе [Создание формы шаблона с помощью объектной модели InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).
    
2. Назовите проект шаблона формы HelloWorld и сохраните его. 
    
   Проектная система создаст файлы кода и проекта, а затем откроет пустой шаблон формы в режиме конструктора InfoPath. Теперь можно добавлять обработчики событий.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Добавление кнопки с обработчиком событий OnClick

1. В разделе **элементы управления** на вкладке **Главная** щелкните элемент управления **Button** , чтобы вставить его в представление. 
    
2. Щелкните правой кнопкой мыши элемент управления и выберите пункт **Свойства кнопки**.
    
3. Измените значение параметра **Метка** на оповещение.
    
4. Измените **идентификатор** на AlertID.
    
5. Нажмите кнопку **Редактировать код формы**.
    
   Созданы каркас обработчика событий для событий [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) и фокус перемещается на редактор кода в Visual Studio 2012. Дополнительные сведения по работе с обработчиков событий можно [Добавить события обработчик с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md). 
    
   Теперь можно добавить код формы для обработчика событий кнопки.
    
### <a name="add-form-code-to-the-event-handler"></a>Добавление кода формы для обработчика событий

1. В обработчике событий **OnClick** введите следующий код: 
    
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
   > В качестве альтернативы, с помощью метода **оповещения** можно использовать метод **MessageBox.Show** пространства имен **System.Windows.Forms** для отображения окна сообщения. Для этого необходимо добавить ссылку на сборку System.Windows.Forms, добавьте `using System.Windows.Forms;` или `Imports System.Windows.Forms` директив в начале файла кода и затем введите строку кода, включая следующие:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Переключитесь в окно режима конструктора InfoPath и затем нажмите кнопку **Просмотр** на вкладке **Главная** . 
    
3. В окне **Просмотр** нажмите кнопку **оповещения** . 
    
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
    
3. В окне InfoPath **Просмотр** нажмите кнопку **оповещения** . 
    
   Фокус перемещается на редактор кода, и выделяется строка точки останова.
    
4. Чтобы продолжить выполнение кода, в меню **Отладка** выберите пункт **Шаг с обходом** (или нажмите сочетание клавиш SHIFT+F8). 
    
   **Оповещения** метод код выполняется и «Hello World!» в окне InfoPath **Просмотр** отобразится оповещение. 
    
## <a name="getting-the-current-users-name"></a>Получение имени текущего пользователя

С помощью классов .NET Framework можно получить доступ к возможностям, которые сложно реализовать в скрипте. В этом примере предоставляется обучение использованию классов .NET Framework для получения имени текущего пользователя.
  
### <a name="add-an-onload-event-handler"></a>Добавление обработчика событий OnLoad

1. Откройте проект InfoPath "HelloWorld", созданный ранее.
    
2. На вкладке **Просмотр** выберите **Отобразить поля**.
    
3. Щелкните правой кнопкой мыши узел **myFields** и нажмите кнопку **Добавить**.
    
4. В поле **имя**введите **employee**и нажмите кнопку **ОК**.
    
5. Перетащите узел **employee** в представление. 
    
6. На вкладке **Разработчик** щелкните **Событие onLoad**.
    
   Это будет создан обработчик событий для события [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) и фокус перемещается в редактор кода. Код в этот обработчик событий вызывается каждый раз, когда загрузки формы. Далее показано, как добавить код формы, который извлекается имя пользователя для обработчика событий. 
    
### <a name="add-form-code"></a>Добавление кода формы 

1. В обработчике событий **OnLoad** введите следующий код: 
    
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
    
   Текстовое поле employee должно теперь выведено текущее имя пользователя. 
    
Сведения о развертывании шаблона форм с управляемым кодом содержатся в разделе [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md). Сведения об объектной модели InfoPath и типичные задачи программирования в шаблонах форм с управляемым кодом, работающих с объектной моделью совместимых с InfoPath 2003 в разделе [Общие сведения об объектной модели InfoPath 2003](understanding-the-infopath-2003-object-model.md). 
  
## <a name="see-also"></a>См. также

- [Инициализация и очистка кода с помощью объектной модели InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [Объектные модели, совместимые с InfoPath 2003](infopath-2003-compatible-object-models.md)
- [Добавление обработчика событий с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

