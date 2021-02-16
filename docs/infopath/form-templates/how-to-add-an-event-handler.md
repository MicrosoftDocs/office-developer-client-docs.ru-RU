---
title: Добавление обработера событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- событие versionupgrade [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], adding event handlers,Sign event [InfoPath 2007],ViewSwitched event [InfoPath 2007],event handling [InfoPath 2007],Merge event [InfoPath 2007],Validating event [InfoPath 2007],Submit event [InfoPath 2007],Save event [InfoPath 2007] ,Loading event [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: В этом разделе описаны процедуры добавления обработчиков событий в шаблон формы Microsoft InfoPath с управляемым кодом с помощью Visual Studio 2012. Чтобы добавить обработщик событий в шаблон формы, необходимо сначала открыть шаблон формы в конструкторе InfoPath, а затем выбрать соответствующую команду пользовательского интерфейса для события, для которое нужно написать код. После выбора команды для события в конструкторе InfoPath фокус автоматически переключается на обработщик события в редакторе кода Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427187"
---
# <a name="add-an-event-handler"></a>Добавление обработера событий

В этом разделе описаны процедуры добавления обработчиков событий в шаблон формы Microsoft InfoPath с управляемым кодом с помощью Visual Studio 2012. Чтобы добавить обработщик событий в шаблон формы, необходимо сначала открыть шаблон формы в конструкторе InfoPath, а затем выбрать соответствующую команду пользовательского интерфейса для события, для которое нужно написать код. После выбора команды для события в конструкторе InfoPath фокус автоматически переключается на обработщик события в редакторе кода Visual Studio 2012.
  
> [!IMPORTANT]
> Для добавления обработщика событий всегда следует использовать пользовательский интерфейс Конструктор InfoPath. Добавление обработчика событий с помощью пользовательского интерфейса приводит к созданию кода привязки события в методе **InternalStartup** файла FormCode.cs или FormCode.vb в проекте шаблона формы. Не следует самостоятельно создавать метод **InternalStartup** или добавлять какой-либо дополнительный код. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Добавление обработчика событий Click для элемента управления "Кнопка"

1. Откройте шаблон формы в конструкторе InfoPath,  а затем добавьте в форму кнопку. 
    
2. Нажмите кнопку, а затем на вкладке **Свойства** ленты выберите **Пользовательский код**.
    
    Фокус переключается на обработок события [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) "Нажми и щелкните" в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Добавление обработчика событий Changing, Validating и Changed для поля или группы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Щелкните правой кнопкой мыши элемент управления ввода данных, связанный с полем или группой, например элемент управления **Текстовое поле**. 
    
3. Щелкните **Программирование** и выберите событие, для которого необходимо создать обработчик. Фокус переключается на обработок события "Изменение", [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) "Проверка" или "Изменен" в редакторе кода Visual Studio 2012. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) 
    
    > [!NOTE]
    > Команда для создания обработчика событий для события **Changing** не будет доступна, если параметр совместимости шаблона формы имеет значение **Форма веб-браузера**. Это происходит потому, что событие **Changing** не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов в Microsoft SharePoint Server 2010 с InfoPath Forms Services. Чтобы создать обработчик события для события **Changing**, необходимо в конструкторе InfoPath изменить параметр совместимости на **Форма редактора InfoPath**. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Добавление обработчика событий Loading, ViewSwitched, ContextChanged и Sign для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. На вкладке **Разработчик** ленты выберите событие формы, для которого требуется написать обработчик событий. 
    
    Фокус переключается на обработчик события "Загрузка", [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) ["ViewSwitched",](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) ["ContextChanged"](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или "Подпись" в редакторе кода Visual Studio 2012. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) 
    
    > [!NOTE]
    > Команды, которые необходимо создать обработник событий [для событий ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) недоступны, если для параметра совместимости шаблона формы установлено "Форма веб-браузера".  Это происходит потому, что эти события не поддерживаются в бизнес-логике шаблонов форм, опубликованных в библиотеках документов в Microsoft SharePoint Server 2010 с InfoPath Forms Services. Чтобы создать обработщик событий [для события ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) необходимо изменить параметр совместимости на "Форма редактора **InfoPath"** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Добавление обработчика событий Submit для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Click the **File** tab, click **Submit To** on the **Info** tab, and then click ** Submit Options **.
    
3. Последовательно щелкните **Разрешить пользователям отправлять эту форму**, **Выполнить пользовательское действие с использованием кода** и **Редактировать код**.
    
    Фокус переключается на обработчитель [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) события "Отправить" в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Добавление обработчика событий Save для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Сохранение**, установите флажок **Сохранить с использованием пользовательского кода**, а затем щелкните **Изменить**.
    
    Фокус переключается на обработок события "Структуры" для события [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе Visual Studio 2012. 
    
    > [!NOTE]
    > Флажок **Сохранить с использованием пользовательского кода** недоступен, если параметр совместимости шаблона формы имеет значение **Службы форм InfoPath**. Это происходит потому, что событие [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов в Microsoft SharePoint Server 2010 с InfoPath Forms Services. Чтобы создать обработщик [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) событий для события "Сохранить", необходимо изменить параметр совместимости на "Форма редактора **InfoPath"** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Добавление обработчика событий VersionUpgrade для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Управление версиями**, выберите вариант **Использовать специальное событие** в раскрывающемся списке **Обновить существующие формы**, а затем щелкните **Изменить**.
    
    Фокус переключается на обработок события "Структуры" для события [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Добавление обработчика событий Merge для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Дополнительно**, установите флажки **Разрешить объединение форм** и **Объединить с использованием пользовательского кода**, а затем щелкните **Изменить**.
    
    Фокус переключается на обработчивую структуры события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) в редакторе Visual Studio 2012. 
    
    > [!NOTE]
    > Если **для параметра** совместимости шаблона формы установлено InfoPath Forms Services, то параметр "Включить **объединение форм" не InfoPath Forms Services.** Это происходит потому, что событие [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов в Microsoft SharePoint Server 2010 с InfoPath Forms Services. Чтобы создать обработщик события [Merge,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) необходимо изменить параметр совместимости на "Форма редактора **InfoPath"** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
## <a name="see-also"></a>См. также



[Walkthrough: Creating a Basic Form Template with Code](walkthrough-creating-a-basic-form-template-with-code.md)

