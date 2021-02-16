---
title: Создание надстройки COM для добавления пользовательских функций в InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, создание надстройки com,InfoPath 2007, добавление пользовательских функций,надстройки COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath поддерживает надстройки для модели COM для расширения возможностей пользователя по редактированию форм. Хотя поддержка надстройки COM была впервые добавлена в InfoPath, другие приложения Office, такие как Microsoft Office Word и Microsoft Office Excel, поддерживают надстройки COM, начиная с Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303789"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Создание надстройки COM для добавления пользовательских функций в InfoPath

Microsoft InfoPath поддерживает надстройки для модели COM для расширения возможностей пользователя по редактированию форм. Хотя поддержка надстройки COM была впервые добавлена в InfoPath, другие приложения Office, такие как Microsoft Office Word и Microsoft Office Excel, поддерживают надстройки COM начиная с Office 2000.
  
Поддержка надстройки COM в InfoPath доступна для среды редактирования форм. Среду разработки форм невозможно расширить с помощью надстройки COM.
  
## <a name="the-idtextensibility2-interface"></a>Интерфейс IDTExtensibility2

Среда редактирования InfoPath обеспечивает поддержку интерфейса **IDTExtensibility2,** который должен быть реализован разработчиками надстроек COM. **IDTExtensibility2** — это объект с двумя интерфейсами, который предоставляет пять методов, которые выступают в качестве событий в среде редактирования. Эти методы позволяют надстройка COM реагировать на условия запуска и завершения работы среды, перечисленные в следующей таблице. 
  
|**Интерфейс**|**Описание**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Возникает при загрузке или выгрузке надстройки в среде.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Возникает при закрытии среды.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Возникает при загрузке надстройки в среде.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Возникает, когда надстройка выгружается из среды.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Возникает, когда среда завершит работу.  <br/> |
   
## <a name="registering-com-add-ins"></a>Регистрация надстройки COM

Все приложения Office, в том числе InfoPath, используют реестр для получения списка надстройок в коллекции COM Add-Ins, для хранения состояния подключения и для хранения сведений о загрузке или запросе. Для надстройки Com InfoPath имя каждой надстройки отображается под следующим ключом:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Для надстроек COM, установленных для использования каждым пользователем клиентского компьютера, ключ реестра находится в окне реестра HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Имя ключа реестра соответствует **progIdAttribute** надстройки и содержит следующие значения. 
  
|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**Строка** <br/> |Имя, которое отображается в диалоговом окне "Надстройки **COM"** и отображается на странице "Надстройки" центра управления **доверием.**   <br/> |
|**Описание** <br/> |**Строка** <br/> |Строка, отображаемая при выборе надстройки в центре **управления доверием.**  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Указывает способ загрузки надстройки COM. Значение может быть комбинацией 0, 1, 2, 8 и 16. Дополнительные сведения см. в таблице ниже.  <br/> |
   
Значение **DWORD для** **LoadBehavior** должно содержать значение, описывающие загрузку надстройки COM в среде редактирования. Значение может быть из приведенной ниже таблицы или комбинацией значений из таблицы. Например, надстройка COM, созданная в Visual Studio 2005, будет иметь **loadBehavior** 3, загруженный при запуске приложения и подключенный. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Отключено. В диалоговом окне надстройки **COM** надстройка будет показана как неактивная.  <br/> |
|1   <br/> |Подключено. Надстройка будет показана как активная в диалоговом окне надстройки **COM.**  <br/> |
|2   <br/> |Загрузка при запуске. Надстройка загружается и подключается при загрузке ведущего приложения.  <br/> |
|8   <br/> |Загрузка по запросу. Надстройка загружается и подключается, когда она требуется хост-приложению, например, когда пользователь нажимает кнопку, использующую функции надстройки.  <br/> |
|16   <br/> |Подключение в первый раз. Надстройка будет загружена и подключена при первом запуске ведущим приложением после регистрации надстройки.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Создание управляемой надстройки COM с Visual Studio 2005 или Visual Studio 2008

Для создания управляемой надстройки COM с помощью Microsoft Visual Studio 2005 или Visual Studio 2008 создайте проект shared Add-In следующим образом: 
  
1. Запустите Visual Studio.
    
2. В меню **Файл** выберите команду **Создать проект**.
    
3. В области **"Типы** проектов" диалоговое окно  "Новый проект" выберите папку "Другие типы проектов", а затем щелкните  **"Возможности для реализации".**
    
4. В области **"Шаблоны"** щелкните **"Общая надстройка".**
    
5. В поле **"Имя"** введите имя проекта. 
    
6. В поле **"Расположение"** введите путь к папке или нажмите кнопку **"Обзор",** выберите путь к папке и нажмите кнопку "ОК".  Появится **мастер общих надстройок.** 
    
7. Нажмите **кнопку** "Далее" в **мастере общих надстройок.** Появится **страница "Выбор языка** программирования". 
    
8. Нажмите **кнопку "Создать надстройки" Visual Basic** нажмите кнопку **"Далее".** Появится **страница "Выбор ведущего приложения".** 
    
9. Отойдите флажки рядом с каждым приложением, кроме **Microsoft InfoPath,** и нажмите кнопку **"Далее".** Появится **страница "Введите имя и описание".** 
    
10. В поле **"Имя** надстройки" введите имя надстройки COM. 
    
11. В поле **"Описание** надстройки" введите описание надстройки COM и нажмите кнопку **"Далее".** Появится **страница Add-In выбора** параметров. 
    
12. Проверьте,  загружается ли надстройка при загрузке ведущего приложения, а надстройка должна быть доступна всем пользователям компьютера, на который она была установлена, а не только **пользователю,** который устанавливает ее поля. 
    
13. Нажмите **кнопку** "Далее", чтобы просмотреть **страницу сводки,** а затем нажмите кнопку **"Готово".**
    
После создания проекта Visual Studio в окне обозревателя решений будут отыто два проекта. Первый проект — это проект надстройки COM; Второй проект — это проект установки для развертывания надстройки COM. Мастер  общих надстроек вставляет ссылку только в библиотеку объектов **Microsoft Office 14.0,** поэтому необходимо вставить ссылку на библиотеку объектов InfoPath, вы предприняв следующие действия.
  
1. Дважды **щелкните "Мой проект",** чтобы отобразить свойства проекта надстройки. Щелкните **вкладку** "Ссылки", чтобы отобразить ссылки, автоматически добавленные в проект. 
    
2. Нажмите **кнопку** "Добавить", чтобы отобразить **диалоговое** окно "Добавить ссылку". 
    
3. На **вкладке COM** дважды щелкните библиотеку типов **Microsoft.InfoPath 2.0** и нажмите кнопку **"ОК".**
    
4. Добавление ссылки на библиотеку типов **Microsoft InfoPath 3.0** также добавляет ссылки на три сборки, которые необходимо удалить: **ADODB,** **MSHTML** и **MSXML2.** В **обозревателе решений** в **области "Ссылки"** щелкните правой кнопкой мыши каждую из этих ссылок и выберите **"Удалить".**
    
## <a name="viewing-the-registry-settings"></a>Просмотр параметров реестра

Чтобы просмотреть параметры реестра, которые будут созданы при установке надстройки COM, выполните следующие действия.
  
1. Щелкните правой кнопкой мыши корневой узел проекта установки в обозревателе решений, выберите "Вид", "Редактор" и **"Реестр".**
    
2. В области слева щелкните "плюс", чтобы развернуть **HKEY_LOCAL_MACHINE,** программное **обеспечение,** **Microsoft,** **InfoPath,** а затем **AddIns.**
    
3. Щелкните имя, соответствующее progID проекта общей **надстройки.**
    
Чтобы изменить любое из этих свойств, щелкните его правой кнопкой  мыши, выберите **"Окно** свойств" и измените поле "Значение" в **окне "Свойства".**
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Компилятор и распространение общих Add-In

Чтобы скомпилировать управляемую надстройку COM для тестирования на компьютере, на котором был разработан проект Shared Add-In, щелкните правой кнопкой мыши корневой узел проекта Shared Add-In в обозревателе решений и выберите "Сборка". Если проект создается без ошибок, можно запустить среду редактирования InfoPath и начать использовать управлия надстройку COM. Если у вас запущен экземпляр InfoPath, закроем его перед построением проекта. Кроме того, может потребоваться открыть диалоговое окно "Надстройки COM", чтобы убедиться, что надстройка COM зарегистрирована. Чтобы открыть диалоговое окно "Надстройки COM", выполните следующие действия.
  
1. Откройте среду редактирования InfoPath. Самый простой способ сделать это — открыть существующий шаблон формы, который создаст новую форму на основе этого шаблона формы.
    
2. Щелкните **"Центр управления** доверием" в меню **"Инструменты".** 
    
3. Щелкните **категорию надстройки** слева. 
    
4. В разделе **"Управление"** в  нижней части диалогового окна центра управления выберите в списке надстройки **COM** и нажмите кнопку "Перейти".  
    
5. В **диалоговом** окне "Надстройки COM" вы увидите имя вашей недавно построенной надстройки, и рядом с ней должен быть свой новый. Если рядом с ней нет ни одного из них, не удалось загрузить надстройку  COM из-за ошибки, которая будет указана в разделе "Поведение при загрузке" диалоговых окна. 
    
Чтобы скомпилировать управляемую надстройку COM для использования на компьютере, не на котором был разработан проект shared Add-In, необходимо предпринять дополнительные действия для защиты кода. Сведения о защите проектов shared Add-In для использования на других компьютерах см. в следующих трех статьях:
  
- [Развертывание управляемых com-Add-Ins в Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Использование решения Shim надстройки COM для развертывания управляемых надстройок COM в Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Изоляция расширений Office с помощью мастера com Shim](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Отсутствие изоляции надстройки COM может привести к утечке памяти и несоставной работы приложения. 
  
> [!NOTE]
> Если .NET Framework или другие необходимые сборки из проекта установки еще не установлены на целевых компьютерах, MSI-файл может установиться неправильно. Кроме того, вы не можете распространять MSI-файл, а затем пытаться установить MSI-файл. Остальные файлы поддержки также необходимо распространять в той же папке, что и исходный MSI-файл, созданный Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Написание кода в надстройки COM

События приложения, происходящие в среде редактирования форм InfoPath, могут быть захвачены надстройка COM. Надстройка COM может использовать следующие события объекта [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) для реагирования на действия пользователей: 
  
|**Событие**|**Описание**|
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
   
Чтобы зафиксировать эти события в надстройке COM, необходимо объявить следующие переменные уровня класса в классе **Connect:** 
  
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

Первая строка привнося универсальный объект **приложения,** полученный надстройой, [к](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) объекту _Application3. Вторая строка привносит **свойство** [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) объекта _Application3 (представленного переменной **InfoPathApplication)** к [объекту ApplicationEvents.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) 
  
Чтобы создать обработчики событий, выберите **InfoPathApplicationEvents** в выпадаемом поле "Имя класса" в верхней части  окна Visual Studio, а затем выберите событие, которое необходимо обработать, в поле "Имя метода" в верхней части Visual Studio окна.  Например, если необходимо контролировать, когда форма сохранена, обрабатывается событие **XDocumentBeforeSave.** При выборе **XDocumentBeforeSave** из выпадаемого имени метода автоматически вставляется следующая процедура:  
  
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

- [Создание надстройки COM Microsoft Office 2000](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Создание управляемой com-Add-Ins Office с Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Работа с процедурами событий IDTExtensibility2](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Создание надстройки Office COM с помощью Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Создание надстройки Office COM с помощью Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Создание Add-Ins InfoPath 2007 с помощью средств Visual Studio 2005 для Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)

