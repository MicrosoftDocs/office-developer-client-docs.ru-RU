---
title: Создание надстройки COM для добавления пользовательских функций в InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007 и Создание надстроек com InfoPath 2007 добавления настраиваемых функций, COM-надстроек [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Расширение пользовательского интерфейса редактирования форм Microsoft InfoPath поддерживает COM-надстройки. Хотя поддержка надстройки COM сначала был добавлен в InfoPath, других приложений Office, таких как Microsoft Office Word и Microsoft Office Excel поддерживают COM-надстроек с момента Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395485"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Создание надстройки COM для добавления пользовательских функций в InfoPath

Расширение пользовательского интерфейса редактирования форм Microsoft InfoPath поддерживает COM-надстройки. Хотя поддержка надстройки COM сначала был добавлен в InfoPath, других приложений Office, таких как Microsoft Office Word и Microsoft Office Excel поддерживают COM-надстроек с момента Office 2000.
  
Поддержка надстройки COM в приложении InfoPath доступна для среды редактирования форм. Среда разработки форм не могут быть расширены с помощью COM-надстройки.
  
## <a name="the-idtextensibility2-interface"></a>Интерфейс IDTExtensibility2

InfoPath, которые среда редактирования обеспечивает поддержку интерфейс **IDTExtensibility2** , который должен быть реализован разработчиками COM Add-которые запускаются **IDTExtensibility2** — это объект двойного интерфейса, который предоставляет пять методов, которые действуют как события в среде редактирования. Эти методы позволяют надстройки COM реагировать на среду запуска и завершения работы условий, перечисленных в следующей таблице. 
  
|**Интерфейс**|**Описание**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() как вариант)** <br/> |Происходит, когда надстройка загрузке или выгрузке в среде.  <br/> |
|**OnBeginShutdown (ByVal custom() как вариант)** <br/> |Возникает при завершении работы среды.  <br/> |
|**OnConnection (ByVal как объект приложения, ByVal ConnectMode как ext_ConnectMode, ByVal AddInInst как объект, ByVal custom() как Variant)** <br/> |Происходит, когда надстройка загружается в среде.  <br/> |
|**OnDisconnection (ByVal RemoveMode как ext_DisconnectMode, ByVal custom() как Variant)** <br/> |Происходит при выгрузке из среды надстройки.  <br/> |
|**OnStartupComplete (ByVal custom() как вариант)** <br/> |Возникает при завершении запуска среды.  <br/> |
   
## <a name="registering-com-add-ins"></a>Регистрация надстройки COM

Все приложения Office, включая InfoPath, с помощью реестра для надстроек списка в коллекции надстройки COM для хранения состояния подключения и хранятся сведения о загрузке загрузки или запросами. Для InfoPath надстройки COM, имя каждой надстройки отображается в следующем разделе:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Для установки надстройки COM для использования с каждого пользователя на клиентском компьютере в разделе реестра находится в кусте реестра HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Имя ключа реестра соответствует **ProgIdAttribute** из надстройки, а также содержит следующие значения. 
  
|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**Строка** <br/> |Имя, которое отображается в диалоговом окне **надстройки COM** и на странице **Add-ins** в **Центр управления безопасностью**.  <br/> |
|**Описание** <br/> |**Строка** <br/> |Строка, которая отображается при выборе надстройки в **Центр управления безопасностью**.  <br/> |
|**LoadBehavior** <br/> |**ЗНАЧЕНИЕ DWORD** <br/> |Указывает способ надстройки COM загружается. Значение может быть сочетание 0, 1, 2, 8 и 16. В приведенной ниже таблице для получения дополнительных сведений.  <br/> |
   
Значение **DWORD** для **LoadBehavior** должны содержать значение, указывающее способ загрузки надстройки COM в среде редактирования. Значение может быть в таблице ниже или сочетание значений из таблицы. Например, надстройки COM, созданные в Visual Studio 2005 будут иметь **LoadBehavior** «3» загрузить при запуске приложения и быть подключен. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Отключен. Надстройки показано, как неактивное в диалоговом окне **надстройки COM** .  <br/> |
|1  <br/> |Подключение. Надстройки показано, как активный в диалоговом окне **надстройки COM** .  <br/> |
|2  <br/> |Загружать при запуске. Надстройка загружен и подключен при запуске ведущего приложения.  <br/> |
|8  <br/> |Загружать по запросу. Надстройка загружен и подключен, когда ведущее приложение необходимо, например, когда пользователь нажимает кнопку, которая использует функциональные возможности надстройки.  <br/> |
|16  <br/> |Подключите первый раз. Надстройка будет загружать и подключена при первом запуске ведущее приложение после регистрации надстройки.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Создание управляемой надстройки COM с помощью Visual Studio 2005 или Visual Studio 2008

Для создания управляемых COM-надстройки с помощью Microsoft Visual Studio 2005 или Visual Studio 2008, создайте проект Общая надстройка следующим образом: 
  
1. Запустите Visual Studio.
    
2. В меню **Файл ** выберите команду **Создать проект **.
    
3. В области **Типы проектов** в диалоговом окне **Создать проект** выберите папку **Другие типы проектов** и нажмите кнопку **расширяемости**.
    
4. В области **Шаблоны** выберите **Общая надстройка**.
    
5. В поле **имя** введите имя для проекта. 
    
6. В поле **расположение** введите путь к папке или нажмите кнопку **Обзор** и выберите путь к папке и нажмите кнопку **ОК**. Откроется **Мастер надстроек Shared** . 
    
7. Нажмите кнопку **Далее** в **общих мастер надстроек**. Откроется страница " **Выбрать язык программирования** ". 
    
8. Нажмите кнопку **Создать надстройку, используя Visual Basic**, а затем нажмите кнопку **Далее**. Откроется страница " **Выберите ведущее приложение** ". 
    
9. Снимите флажки рядом с пунктом каждого приложения, за исключением **Microsoft InfoPath**и нажмите кнопку **Далее**. Откроется страница " **Введите имя и описание** ". 
    
10. В поле **имя надстройки** введите имя для надстройки COM. 
    
11. В поле **Описание - in** введите описание для надстройки COM и нажмите кнопку **Далее**. Откроется страница " **Выберите параметры надстройки** ". 
    
12. Проверьте, **как надстройку во время запуска ведущего приложения загрузки** и **надстройку во должны быть доступны для всех пользователей компьютера, на котором установлена на не только человека, который устанавливает** окон. 
    
13. Нажмите кнопку **Далее** для просмотра на странице **Сводка** , а затем нажмите кнопку **Готово**.
    
После создания проекта в Visual Studio, вы увидите два проекта в окне Обозреватель решений. Первый проект — это проект для надстройки COM; второй — проект программы установки для развертывания надстройки COM. **Shared Add-in Wizard** только вставляет ссылки на **Библиотеку объектов Microsoft Office 14.0**, поэтому необходимо вставить ссылку на библиотеку объектов Microsoft InfoPath, выполнив следующие действия:
  
1. Дважды щелкните **Мой проект** для отображения свойств проекта надстройки. Перейдите на вкладку **ссылки** для отображения справочных материалов, автоматически добавляется в проект. 
    
2. Нажмите кнопку **Добавить** , чтобы открыть диалоговое окно **Добавить ссылку** . 
    
3. На вкладке **COM** дважды щелкните **Библиотека типов Microsoft.InfoPath 2.0**и нажмите **кнопку ОК**.
    
4. Добавление ссылки на **Библиотеку типа Microsoft InfoPath 3.0** также добавляет ссылки на три сборки, которые должны быть удалены: **ADODB**, **MSHTML**и **MSXML2 описывается**. В **Обозревателе решений** в области **справочных материалов**щелкните правой кнопкой мыши каждый из этих ссылок и нажмите кнопку **Удалить**.
    
## <a name="viewing-the-registry-settings"></a>Просмотр параметров реестра

Чтобы просмотреть параметры реестра, которые будут созданы при установке надстройки COM, выполните следующие действия:
  
1. Щелкните правой кнопкой мыши корневой узел проекта установки в **Окне Обозреватель решений**, нажмите кнопку **Просмотр**, затем **редактора**, затем нажмите кнопку **реестра**.
    
2. В левой области нажмите знак плюс разверните **HKEY_LOCAL_MACHINE**, **программное обеспечение**, **Корпорация Майкрософт**, **InfoPath**, а затем **AddIns**.
    
3. Выберите имя, соответствующее общей надстройки проекта **ProgID**.
    
Изменение любого из этих свойств, щелкните правой кнопкой мыши свойство, щелкните **Окно "Свойства"** и введите **значение** в **Окно "Свойства"**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Компиляция и распространение общей надстройкой

Для компиляции управляемой надстройки COM для тестирования на компьютере, на котором был разработан project Общая надстройка, щелкните правой кнопкой мыши корневой узел Общая надстройка проекта в обозревателе решений и выберите построение. При построении проекта без ошибок, можно начать среды редактирования InfoPath и начать с помощью управляемой надстройки COM. Если у вас есть экземпляр InfoPath под управлением, закройте его перед построением проекта. Он также может потребоваться открыть диалоговое окно надстройки COM, чтобы убедиться, что надстройка COM зарегистрирован. Чтобы открыть диалоговое окно надстройки COM, выполните следующие действия:
  
1. Откройте среды редактирования InfoPath. Для этого проще всего открыть существующего шаблона формы, которая создаст новую форму на основе этого шаблона формы.
    
2. В меню **Сервис** щелкните **Центр управления безопасностью** . 
    
3. Выберите категорию **надстройки** слева. 
    
4. В разделе **Управление** в нижней части диалогового окна **Центр управления безопасностью** выберите **надстройки COM** в списке и нажмите кнопку **Перейти** . 
    
5. В диалоговом окне **надстройки COM** появится имя надстройки недавно созданных и должен появиться флажок рядом с ним. Если флажок рядом с ним, надстройки COM не удалось загрузить из-за ошибки, которое указывается в разделе **Поведение загрузки** диалогового окна. 
    
Чтобы компилировать управляемой надстройки COM для использования на компьютере, отличных от компьютера, на котором был разработан Общая надстройка project, необходимо выполнить дополнительные действия для обеспечения безопасности кода. Сведения о защите проекты Общая надстройка для использования на других компьютерах, просмотрите следующие три статьи:
  
- [Развертывание из управляемых надстроек COM в Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Использование решений оболочки совместимости надстройки COM для развертывания управляемых надстроек COM в Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Изолирование расширений Microsoft Office с помощью мастера COM Shim](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Не изоляция надстройки COM может стать причиной утечки памяти и нестабильности приложения. 
  
> [!NOTE]
> Если .NET Framework или другие необходимые сборки из проекта установки не уже установлены на конечных компьютерах, MSI-файл может установлен неправильно. Кроме того нельзя распространение MSI-файл и затем предпринята попытка установить MSI-файл. Необходимо также передать другие файлы поддержки в той же папке, что исходный файл MSI-файла, созданные приложением Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Написание кода в надстройки COM

События приложения, которые происходят в редактора форм InfoPath можно записаны с COM-надстройки. Можно использовать следующие события объекта [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) , надстройка COM реагировать на действия пользователя: 
  
|**Событие**|**Описание**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Событие  <br/> |Происходит при создании новой формы.  <br/> |
|[Завершите работу](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Событие  <br/> |Происходит, когда пользователь покидает InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Событие  <br/> |Происходит при активации любого окна документа.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Событие  <br/> |Происходит при отключении любого окна документа.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Событие  <br/> |Происходит при изменении размера или перемещении любого окна документа.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Событие  <br/> |Происходит непосредственно перед закрытием любого открытого документа.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Событие  <br/> |Происходит непосредственно перед печатью любого открытого документа.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Событие  <br/> |Происходит непосредственно перед сохранением любого открытого документа.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Событие  <br/> |Происходит при создании новой формы, при открытии существующей формы или при активировании другой формы.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Событие  <br/> |Происходит при открытии документа.  <br/> |
   
Для записи этих событий в надстройки COM, необходимо объявить следующие переменные уровня класса в классе **Connect** : 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

Первая строка приводит универсальное приложение, **объект** , получаемые добавить в объект [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) . Во второй строке приводит свойства [событий](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) объекта **_Application3** (представленное переменной **InfoPathApplication** ) объект [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Создание обработчиков событий, выберите **InfoPathApplicationEvents** из раскрывающегося списка **Имя класса** в верхней части окна Visual Studio и выберите события, которое вы хотите обрабатывать в раскрывающемся списке **Имя метода** в верхней части визуального Окно Studio. К примеру Если вам нужно управлять при сохранении формы, обрабатывать события **XDocumentBeforeSave** . При выборе **XDocumentBeforeSave** из раскрывающегося списка **Имя метода** автоматически вставляется следующую процедуру: 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

Какие-либо события объекта **ApplicationEvents** могут быть обработаны с надстройки COM тем же способом. 
  
## <a name="see-also"></a>См. также

- [Создание Microsoft Office 2000 надстройки COM](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Создание Office управляемых COM-надстроек с помощью Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Работа с IDTExtensibility2 процедуры событий](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Построение Office надстройки COM с помощью Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Создание надстройки COM для Microsoft Office с помощью Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Создание надстроек 2007 InfoPath с помощью Visual Studio 2005 Tools for the Office System SE (en)](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

