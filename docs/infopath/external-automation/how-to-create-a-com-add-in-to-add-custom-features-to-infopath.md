---
title: Создание надстройки COM для добавления настраиваемой функции в InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, создание надстройок com,InfoPath 2007, добавление пользовательских функций, надстройки COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath поддерживает надстройки для модели COM для расширения возможностей пользователя по редактированию форм. Хотя поддержка надстройок COM впервые была добавлена в InfoPath, другие приложения Office, такие как Microsoft Office Word и Microsoft Office Excel, поддерживают надстройки COM с Office 2000 г.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303789"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Создание надстройки COM для добавления настраиваемой функции в InfoPath

Microsoft InfoPath поддерживает надстройки для модели COM для расширения возможностей пользователя по редактированию форм. Хотя поддержка надстройок COM впервые была добавлена в InfoPath, другие приложения Office, такие как Microsoft Office Word и Microsoft Office Excel, поддерживают надстройки COM с Office 2000 г.
  
Поддержка надстройки COM в InfoPath доступна для среды редактирования форм. Невозможно расширить среду разработки формы с помощью надстройок COM.
  
## <a name="the-idtextensibility2-interface"></a>Интерфейс IDTExtensibility2

Среда редактирования InfoPath обеспечивает поддержку интерфейса **IDTExtensibility2,** который должен быть реализован разработчиками надстроек COM. **IDTExtensibility2** — это объект с двойным интерфейсом, который предоставляет пять методов, которые выступают в качестве событий в среде редактирования. Эти методы позволяют надстройку COM реагировать на условия запуска и остановки среды, перечисленные в следующей таблице. 
  
|**Интерфейс**|**Описание**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Возникает при загрузке или разгрузке надстройки в среде.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Возникает при закрытии среды.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Возникает при загрузке надстройки в среде.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Возникает при выгрузке надстройки из среды.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Происходит, когда среда завершила запуск.  <br/> |
   
## <a name="registering-com-add-ins"></a>Регистрация надстройок COM

Все Office, включая InfoPath, используют реестр для списка надстройок в коллекции COM Add-Ins, хранения состояния подключения и хранения данных загрузки или загрузки. Для надстройок InfoPath COM имя каждой надстройки отображается под следующим ключом:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Для надстроек COM, установленных для использования каждым пользователем клиентского компьютера, ключ реестра расположен в улье реестра HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Имя ключа реестра соответствует **progIdAttribute** надстройки и содержит следующие значения. 
  
|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Имя, отображаемого в диалоговом окне **надстройки COM** и перечисленное на странице надстройки Центра  **доверия.**  <br/> |
|**Описание** <br/> |**Строка** <br/> |Строка, отображаемая при выборе надстройки в Центре **доверия.**  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Указывает способ загрузки надстройки COM. Значение может быть сочетанием 0, 1, 2, 8 и 16. Дополнительные сведения см. в таблице ниже.  <br/> |
   
Значение **DWORD** для **LoadBehavior** должно содержать значение, описывающие нагрузки надстройки COM в среде редактирования. Значение может быть из приведенной ниже таблицы или сочетания значений из таблицы. Например, надстройка COM, созданная в 2005 Visual Studio 2005 г., будет иметь **loadBehavior** "3", загруженную при запуске приложения и подключенную. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Отключено. Надстройка показана как Неактивно в диалоговом окне надстройки **COM.**  <br/> |
|1  <br/> |Подключено. Надстройка показана как Active в диалоговом окне надстройки **COM.**  <br/> |
|2  <br/> |Загрузка в Startup. Надстройка загружается и подключается, когда запускается хост-приложение.  <br/> |
|8   <br/> |Загрузка по запросу. Надстройка загружается и подключается, когда это требуется хост-приложению, например, когда пользователь щелкает кнопку, использующую функции надстройки.  <br/> |
|16   <br/> |Подключение первый раз. Надстройка будет загружена и подключена при первом запуске приложения-хост после регистрации надстройки.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Создание надстройки managed COM с Visual Studio 2005 или Visual Studio 2008 г.

Чтобы создать управляемый надстройки com с Microsoft Visual Studio 2005 или Visual Studio 2008 г., создайте проект shared Add-In следующим образом: 
  
1. Запустите Visual Studio.
    
2. В меню **Файл** выберите команду **Создать проект**.
    
3. В области **Project типов** диалоговое **окно New Project** нажмите папку **Другие** типы проектов, а затем нажмите **extensibility**.
    
4. В области **Шаблоны** нажмите кнопку **Общие надстройки**.
    
5. В поле **Имя** введите имя для проекта. 
    
6. В поле **Расположение** введите путь папки или щелкните **Обзор** и выберите путь папки, а затем нажмите **кнопку ОК**. Появляется **мастер общей надстройки.** 
    
7. Нажмите **кнопку Далее** в **мастере общей надстройки**. Отображается **страница Выберите язык программирования.** 
    
8. Нажмите **кнопку Создать надстройки** с помощью Visual Basic, а затем нажмите **кнопку Далее**. Отображается **страница Выбор хост-приложения.** 
    
9. Отойдите от полей рядом с каждым приложением, кроме **Microsoft InfoPath,** и нажмите **кнопку Далее**. Отображается **страница Введите имя и описание.** 
    
10. В **поле What is the name of your Add-In** box, type the name of your COM add-in. 
    
11. В поле **What is the description of your Add-In** box, type the description for your COM add-in, and click **Next**. Отображается **страница Add-In Параметры.** 
    
12. Проверьте, как загружается надстройка, когда загрузка **хост-приложения** и надстройка **My Add-in** должны быть доступны всем пользователям установленного компьютера, а не только человеку, который устанавливает его ящики. 
    
13. Нажмите **кнопку Далее,** чтобы просмотреть **страницу Сводка,** а затем нажмите **кнопку Готово**.
    
После создания проекта Visual Studio вы увидите два проекта в окне Обозреватель решений. Первый проект — это проект надстройки COM; Второй проект — это проект установки для развертывания надстройки COM. Мастер  общих надстроек вставляет ссылку только на объектную библиотеку **14.0** Microsoft Office, поэтому необходимо вставить ссылку на объектную библиотеку InfoPath с помощью следующих действий:
  
1. Дважды нажмите **кнопку Project,** чтобы отобразить свойства проекта надстройки. Щелкните **вкладку Ссылки,** чтобы отобразить ссылки, автоматически добавленные в проект. 
    
2. Нажмите **кнопку Добавить,** чтобы отобразить диалоговое окно **Add Reference.** 
    
3. На **вкладке COM** дважды щелкните Библиотеку типов **Microsoft.InfoPath 2.0** и нажмите **кнопку ОК.**
    
4. Добавление ссылки на библиотеку типов **Microsoft InfoPath 3.0** также добавляет ссылки на три сборки, которые необходимо удалить: **ADODB,** **MSHTML** и **MSXML2.** В **обозревателе решений** в **статье Ссылки** щелкните правой кнопкой мыши каждую из этих ссылок и нажмите кнопку **Удалить**.
    
## <a name="viewing-the-registry-settings"></a>Просмотр реестра Параметры

Чтобы просмотреть параметры реестра, созданные при установке надстройки COM, выполните следующие действия:
  
1. Щелкните правой кнопкой мыши корневой узел проекта установки в обозревателе решений **,** нажмите кнопку **Просмотр**, затем **редактор**, а затем нажмите **кнопку Реестр**.
    
2. В левой области нажмите кнопку плюс, чтобы расширить **HKEY_LOCAL_MACHINE ,** программное **обеспечение**, **Microsoft**, **InfoPath**, а затем **AddIns**.
    
3. Щелкните имя, соответствующее progID проекта общей **надстройки.**
    
Чтобы изменить любое из этих свойств, щелкните свойство правой кнопкой мыши, нажмите **кнопку Properties Window** и измените поле **Значение** в **окне Свойства**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Компилятор и распространение общих Add-In

Для компиляции управляемой надстройки com для тестирования на компьютере, на котором был разработан проект Shared Add-In, щелкните правой кнопкой мыши корневой узел проекта Shared Add-In в обозревателе решений и нажмите кнопку Сборка. Если проект строится без ошибок, можно запустить среду редактирования InfoPath и приступить к использованию управляемой надстройки COM. Если запущен экземпляр InfoPath, закрой его перед созданием проекта. Кроме того, может потребоваться открыть диалоговое окно надстройки COM, чтобы убедиться, что надстройка COM зарегистрирована. Чтобы открыть диалоговое окно надстроек COM, выполните следующие действия:
  
1. Откройте среду редактирования InfoPath. Самый простой способ сделать это — открыть существующий шаблон формы, который создаст новую форму на основе этого шаблона формы.
    
2. Щелкните **Центр доверия** в меню **Tools.** 
    
3. Щелкните **категорию надстройки** слева. 
    
4. В разделе **Управление** в нижней части диалогового окна Центра доверия выберите  **надстройки COM** из списка и нажмите кнопку **Перейти.** 
    
5. В **диалоговом** окне надстройки COM вы увидите имя недавно построенной надстройки, рядом с ней должна быть проверка. Если рядом нет контрольного окна, надстройка COM не была загружена из-за ошибки, которая будет указана в разделе **Поведение** нагрузки в диалоговом окне. 
    
Для компиляции управляемой надстройки com для использования на компьютере, помимо компьютера, на котором был разработан проект shared Add-In, необходимо предпринять дополнительные действия для обеспечения безопасности кода. Сведения о защите общих Add-In проектов для использования на других компьютерах см. в следующих трех статьях:
  
- [Развертывание управляемых Add-Ins в Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Использование решения Shim надстройки COM для развертывания управляемых надстройок COM в Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Изолирование Office расширений с мастером COM Shim](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Отсутствие изоляции надстройки COM может привести к утечкам памяти и нестабильности приложений. 
  
> [!NOTE]
> Если платформа .NET Framework или другие необходимые сборки из проекта установки еще не установлены на целевых компьютерах, .msi файл может не установиться должным образом. Кроме того, нельзя распространять .msi файл, а затем пытаться установить .msi файл. Необходимо также распространять другие файлы поддержки в той же папке, что и исходный .msi, созданный Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Кодирование в надстройки COM

События приложения, происходящие в среде редактирования форм InfoPath, могут быть захвачены надстройком COM. Следующие события объекта [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) могут использоваться надстройка COM для реагирования на действия пользователей: 
  
|**Event**|**Описание**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Событие  <br/> |Происходит при создании новой формы.  <br/> |
|[Quit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Событие  <br/> |Происходит, когда пользователь покидает InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Событие  <br/> |Происходит при активации любого окна документа.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Событие  <br/> |Происходит при отключении любого окна документа.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Событие  <br/> |Происходит при изменении размера или перемещении любого окна документа.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Событие  <br/> |Происходит непосредственно перед закрытием любого открытого документа.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Событие  <br/> |Происходит непосредственно перед печатью любого открытого документа.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Событие  <br/> |Происходит непосредственно перед сохранением любого открытого документа.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Событие  <br/> |Происходит при создании новой формы, при открытии существующей формы или при активировании другой формы.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Событие  <br/> |Происходит при открытии документа.  <br/> |
   
Чтобы зафиксировать эти события в надстройке COM, необходимо объявить следующие переменные уровня класса **в Подключение** классе: 
  
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

В первой строке отбрасывется общий **объект** приложения, полученный надстройка, [к объекту _Application3.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) Вторая строка отбрасирует **свойство** [События](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) объекта _Application3 (представленная переменной **InfoPathApplication)** в объект [ApplicationEvents.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) 
  
Чтобы создать обработчики событий, выберите **InfoPathApplicationEvents** из выпадаемого окна Имя класса в верхней части  окна Visual Studio, а затем выберите событие, которое необходимо обработать в выпадаемом окне Имя метода в верхней Visual Studio окне.  Например, если необходимо контролировать, когда форма сохранена, вы обрабатываете **событие XDocumentBeforeSave.** Выбор **XDocumentBeforeSave** из  выпадения имен метода автоматически вставляет следующую процедуру: 
  
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

Любое из событий объекта **ApplicationEvents** можно обрабатывать с помощью надстройки COM с помощью того же метода. 
  
## <a name="see-also"></a>См. также

- [Создание надстройки Microsoft Office 2000 COM](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Создание Office com Add-Ins с Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Работа с процедурами событий IDTExtensibility2](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Создание надстройки Office COM с Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Создание надстройки Office com с помощью Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Создание InfoPath 2007 Add-Ins с помощью Visual Studio 2005 для Office системы SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

