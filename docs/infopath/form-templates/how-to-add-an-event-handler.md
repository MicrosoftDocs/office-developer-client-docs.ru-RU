---
title: Добавление обработка событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007], обработка событий [InfoPath 2007], Изменение события [InfoPath 2007], InfoPath 2007, добавление обработчиков событий, измененное событие [InfoPath 2007], Событие ContextChanged [InfoPath 2007], Щелкните событие [InfoPath 2007], события [InfoPath 2007], добавление обработчиков событий, событие Sign [InfoPath 2007],ViewSwitched event [InfoPath 2007], обработка событий [InfoPath 2007], событие Слияния [InfoPath 2007], проверка события [InfoPath 2007], Отправка события [InfoPath 2007] ,Сохраните событие [InfoPath 2007], событие загрузки [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: В этом разделе описаны процедуры добавления обработчиков событий в шаблон управляемых форм кода Microsoft InfoPath с Visual Studio 2012 г. Чтобы добавить обработщик событий в шаблон формы, сначала откройте шаблон формы в конструкторе InfoPath, а затем выберите соответствующую команду пользовательского интерфейса для события, для чего нужно написать код. После выбора команды события в конструкторе InfoPath фокус автоматически переключается на обработщик событий скелета для этого события в редакторе кода Visual Studio 2012 года.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427187"
---
# <a name="add-an-event-handler"></a>Добавление обработка событий

В этом разделе описаны процедуры добавления обработчиков событий в шаблон управляемых форм кода Microsoft InfoPath с Visual Studio 2012 г. Чтобы добавить обработщик событий в шаблон формы, сначала откройте шаблон формы в конструкторе InfoPath, а затем выберите соответствующую команду пользовательского интерфейса для события, для чего нужно написать код. После выбора команды события в конструкторе InfoPath фокус автоматически переключается на обработщик событий скелета для этого события в редакторе кода Visual Studio 2012 года.
  
> [!IMPORTANT]
> Для добавления обработщика событий всегда следует использовать пользовательский интерфейс Конструктор InfoPath. Добавление обработчика событий с помощью пользовательского интерфейса приводит к созданию кода привязки события в методе **InternalStartup** файла FormCode.cs или FormCode.vb в проекте шаблона формы. Не следует самостоятельно создавать метод **InternalStartup** или добавлять какой-либо дополнительный код. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Добавление обработчика событий Click для элемента управления "Кнопка"

1. Откройте шаблон формы в конструкторе InfoPath  и добавьте в форму кнопку управления. 
    
2. Нажмите кнопку, а затем на вкладке **Свойства** ленты выберите **Пользовательский код**.
    
    Фокус переключается на обработник событий скелета для события [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) в редакторе кода 2012 Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Добавление обработчика событий Changing, Validating и Changed для поля или группы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Щелкните правой кнопкой мыши элемент управления ввода данных, связанный с полем или группой, например элемент управления **Текстовое поле**. 
    
3. Щелкните **Программирование** и выберите событие, для которого необходимо создать обработчик. Фокус переключается на обработчитель событий скелета для [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) события [Изменения,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) [Проверки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) или Изменения в редакторе кода 2012 Visual Studio 2012 года. 
    
    > [!NOTE]
    > Команда для создания обработчика событий для события **Changing** не будет доступна, если параметр совместимости шаблона формы имеет значение **Форма веб-браузера**. Это происходит из-за того, что событие **Changing** не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 г. с InfoPath Forms Services. Чтобы создать обработчик события для события **Changing**, необходимо в конструкторе InfoPath изменить параметр совместимости на **Форма редактора InfoPath**. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Добавление обработчика событий Loading, ViewSwitched, ContextChanged и Sign для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. На вкладке **Разработчик** ленты выберите событие формы, для которого требуется написать обработчик событий. 
    
    Фокус переключается на обработчик событий скелета для редактора кода [Loading,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) [ViewSwitched,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) Visual Studio 2012. 
    
    > [!NOTE]
    > Команды по созданию обработчицы событий для событий [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) недоступны, если параметр совместимости шаблона формы установлен в **форме веб-браузера.** Это происходит из-за того, что эти события не поддерживаются в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 г. с InfoPath Forms Services. Чтобы создать обработщик событий для [события ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) необходимо изменить параметр совместимости на **форму редактора InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Добавление обработчика событий Submit для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Щелкните **вкладку File,** **нажмите Кнопку Отправить на** вкладке **Info** и нажмите кнопку ** Отправка параметров **.
    
3. Последовательно щелкните **Разрешить пользователям отправлять эту форму**, **Выполнить пользовательское действие с использованием кода** и **Редактировать код**.
    
    Фокус переключается на обработник событий скелета для события [Отправка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) в редакторе кода Visual Studio 2012 года. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Добавление обработчика событий Save для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Сохранение**, установите флажок **Сохранить с использованием пользовательского кода**, а затем щелкните **Изменить**.
    
    Фокус переключается на обработник событий скелета для события [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе кода 2012 Visual Studio 2012. 
    
    > [!NOTE]
    > Флажок **Сохранить с использованием пользовательского кода** недоступен, если параметр совместимости шаблона формы имеет значение **Службы форм InfoPath**. Это происходит из-за того, что событие [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 года с InfoPath Forms Services. Чтобы создать обработщик событий для события [Сохранить,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) необходимо изменить параметр совместимости на **форму редактора InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Добавление обработчика событий VersionUpgrade для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Управление версиями**, выберите вариант **Использовать специальное событие** в раскрывающемся списке **Обновить существующие формы**, а затем щелкните **Изменить**.
    
    Фокус переключается на обработник событий скелета для события [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе кода 2012 Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Добавление обработчика событий Merge для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Дополнительно**, установите флажки **Разрешить объединение форм** и **Объединить с использованием пользовательского кода**, а затем щелкните **Изменить**.
    
    Фокус переключается на обработник событий скелета для события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) в редакторе кода Visual Studio 2012 года. 
    
    > [!NOTE]
    > Поле **"Включить объединение форм"** недоступно, если параметр совместимости шаблона формы установлен **InfoPath Forms Services**. Это происходит из-за того, что событие [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 г. с InfoPath Forms Services. Чтобы создать обработщик событий для события [Merge,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) необходимо изменить параметр совместимости на **форму редактора InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
## <a name="see-also"></a>См. также



[Погон: создание базового шаблона формы с кодом](walkthrough-creating-a-basic-form-template-with-code.md)

