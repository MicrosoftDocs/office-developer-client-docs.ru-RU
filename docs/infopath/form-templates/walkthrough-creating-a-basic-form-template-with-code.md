---
title: 'ПоШаговое руководство: создание базового шаблона формы с кодом'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], creating managed code,managed code form templates [InfoPath 2007], creating,form templates [InfoPath 2007], walkthroughs,InfoPath 2007, walkthroughs
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Бизнес-логику для приложения Microsoft InfoPath можно написать на языке Visual Basic или C#, открыв шаблон формы в конструкторе InfoPath и воспользовавшись одной из команд интерфейса пользователя для добавления обработчика событий, который откроет набор Visual Studio 2012 для написания необходимого кода.
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299736"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>ПоШаговое руководство: создание базового шаблона формы с кодом

Бизнес-логику для приложения Microsoft InfoPath можно написать на языке Visual Basic или C#, открыв шаблон формы в конструкторе InfoPath и воспользовавшись одной из команд интерфейса пользователя для добавления обработчика событий, который откроет набор Visual Studio 2012 для написания необходимого кода. По умолчанию проекты шаблонов форм создаются с помощью набора средств Visual Studio 2012, использующего новую объектную модель управляемого кода, которая предоставляется пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
В первом пошаговом руководстве демонстрируются методы создания простого приложения "Hello World" с помощью языка C# или Visual Basic в наборе Visual Studio 2012. В заключении руководства приведен пример кода, демонстрирующий принципы использования свойства [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) для получения имени текущего пользователя и заполнения элемента управления **Текстовое поле** полученным значением. 
  
## <a name="prerequisites"></a>Необходимые компоненты

Для выполнения инструкций этого пошагового руководства в наборе Visual Studio 2012 необходимо установить следующее программное обеспечение:
  
- Microsoft InfoPath с набором Visual Studio 2012.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Создание примера "Hello World" в наборе средств Visual Studio Tools для работы с приложениями

В следующем пошаговом руководстве демонстрируется, как написать в наборе Visual Studio 2012 код, отображающий простое диалоговое окно с оповещением путем написания обработчика события [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) класса [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , связанного с элементом управления **Кнопка**. 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Создание нового проекта и выбор языка программирования

1. Запустите конструктор InfoPath и дважды щелкните шаблон формы **Пустой (редактор InfoPath)**. 
    
2. Чтобы выбрать язык программирования, нажмите кнопку **Microsoft Office**, выберите **Параметры форм**, в списке **Категории** выберите **Программирование**, а затем выберите либо **Visual Basic**, либо **C#** в раскрывающемся списке **Язык кода шаблона формы**. 
    
   > [!NOTE]
   > [!Примечание] При выборе других вариантов языков программирования в списке **Язык кода шаблона формы** обеспечивается совместимость с более ранними версиями InfoPath. Варианты **C# (совместимый с InfoPath 2007)** и **Visual Basic (совместимый с InfoPath 2007)** работают с соблюдением описанных здесь процедур. Однако дополнительные сведения об использовании **C# (совместимый с InfoPath 2003)** и **Visual Basic (совместимый с InfoPath 2003)** см. в разделе [Пошаговое руководство. Создание и отладка начального шаблона формы с помощью объектной модели InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Теперь можно добавить элемент управления **Кнопка** и создать для него обработчик событий. 
    
### <a name="add-a-button-control-and-event-handler"></a>Добавление элемента управления "Кнопка" и обработчика событий

1. В группе **Элементы управления** нажмите элемент управления **Кнопка**, чтобы добавить его в форму. 
    
2. Дважды щелкните элемент управления **Кнопка**, введите значение Hello для свойства **Надпись** на вкладке **Свойства** ленты и щелкните **Пользовательский код**. При получении запроса сохраните форму и назовите ее HelloWorld.
    
   После этого откроется среда **Набор средств Microsoft Visual Studio для работы с приложениями** с курсором на обработчике событий [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) для элемента управления **Кнопка**. 
    
   Теперь можно добавить код формы для обработчика событий кнопки. 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>Добавьте в обработчик событий код "Hello World" и просмотрите форму

1. В структуре обработчика событий введите:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Код в шаблоне формы должен выглядеть примерно следующим образом:
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. Переключитесь в окно режима конструктора InfoPath.
    
3. Нажмите кнопку **Просмотр** на панели инструментов **Главная**. 
    
4. Нажмите на форме кнопку Hello. 
    
   Отобразится окно с текстовым сообщением "Hello World!"
    
   В следующей процедуре показано, как добавить отладочные точки останова в код формы.
    
### <a name="debug-form-code"></a>Отладка кода формы

1. Переключитесь обратно в окно набора Visual Studio 2012.
    
2. Щелкните серую полосу слева от строки:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Отобразится красный кружок, а строка кода будет выделена, указывая, что при запуске кода формы возникнет пауза в этой точке останова.
    
3. В меню **Отладка** выберите пункт **Начать отладку** (или нажмите клавишу F5). 
    
4. В окне InfoPath **Просмотр** нажмите кнопку Hello на форме. 
    
5. Фокус переместится на редактор кода набора Visual Studio 2012 и выделится строка точки останова.
    
6. Чтобы продолжить выполнение кода, в меню **Отладка** выберите пункт **Шаг с обходом** (или нажмите сочетание клавиш SHIFT+F8). 
    
7. Выполнится код обработчика событий, и отобразится сообщение "Hello World!". 
    
8. Нажмите кнопку **ОК**, чтобы вернуться в редактор кода набора Visual Studio 2012, а затем щелкните **Остановить отладку** в меню **Отладка** (или нажмите сочетание клавиш CTRL+ALT+BREAK). 
    
## <a name="getting-the-current-users-name"></a>Извлечение имени текущего пользователя

В следующем примере демонстрируется, как использовать свойство [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) для получения имени текущего пользователя и заполнения значения элемента управления **Текстовое поле** с помощью обработчика событий [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
Заполнение элемента управления **Текстовое поле** выполняется с помощью экземпляра класса [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) для написания имени текущего пользователя в узле XML, к которому привязан элемент управления. 
  
Сначала свойство [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) вызывается для получения экземпляра класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , представляющего базовый XML-документ формы. Затем объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) вызывает метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , создающий объект **XPathNavigator** и размещающий его в корневом узле основного источника данных формы. 
  
Метод [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) класса **XPathNavigator** вызывается для выбора поля employee в источнике данных формы. В заключение вызывается метод [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) для установки значения поля с использованием свойства [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) . 
  
Дополнительные сведения о работе с **System. XML** в шаблонах форм с управляемым кодом приведены в статье [Работа с классами XPathNavigator и XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="add-a-loading-event-handler"></a>Добавление обработчика событий загрузки

1. Откройте шаблон формы "HelloWorld", созданный в предыдущем пошаговом руководстве.
    
2. На вкладке **Просмотр** выберите **Отобразить поля**.
    
3. Щелкните правой кнопкой мыши папку **myFields**, а затем выберите **Добавить**.
    
4. В поле **Имя** введите значение employee и нажмите кнопку **ОК**.
    
5. Перетащите поле employee в текущее представление. 
    
6. На вкладке **Разработчик** щелкните **Событие "Загрузка"**.
    
   При этом будет создан обработчик событий [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , а фокус переключится на этот обработчик событий в редакторе кода. 
    
7. В редакторе кода введите следующее:
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. Переключитесь в окно конструктора форм InfoPath и нажмите кнопку **Просмотр** на вкладке **Главная**, чтобы просмотреть форму. 
    
   В поле employee должно быть автоматически введено имя пользователя. 
    
## <a name="next-steps"></a>Дальнейшие действия

- Сведения о работе с обработчиками событий для других элементов управления и событий можно найти [в статье Добавление обработчика событий](how-to-add-an-event-handler.md).
    
- Для получения дополнительных сведений о предварительном просмотре и отладке кода в шаблонах форм, ознакомьтесь со статьей [Просмотр и отладка шаблонов форм InfoPath с кодом](how-to-preview-and-debug-infopath-form-templates-with-code.md).
    
- Сведения о развертывании шаблона формы с управляемым кодом можно найти в статье [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md).
    
- Сведения об объектной модели InfoPath и распространенных задачах программирования для шаблонов форм с управляемым кодом см. в разделе [Ознакомление с объектной моделью InfoPath и распространенными задачами разработчиков](understanding-the-infopath-object-model-and-common-developer-tasks.md)
    
## <a name="see-also"></a>См. также

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

