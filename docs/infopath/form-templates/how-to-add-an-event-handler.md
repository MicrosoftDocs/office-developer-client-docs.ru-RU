---
title: Добавление обработчика событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- событие VersionUpgrade [InfoPath 2007], обработка событий [InfoPath 2007], изменение события [InfoPath 2007], InfoPath 2007, добавление обработчиков событий, события изменения [InfoPath 2007], событие ContextChanged [InfoPath 2007], события [InfoPath 2007], события [InfoPath 2007], добавление обработчиков событий, табличного события [InfoPath 2007], событие ViewSwitched [InfoPath 2007], обработка событий [InfoPath 2007], событие Merge [InfoPath 2007], проверка события [InfoPath 2007], событие "послать" [InfoPath 2007], событие Save [InfoPath 2007] , Загрузка события [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: В этом разделе описываются процедуры добавления обработчиков событий в шаблон формы с управляемым кодом Microsoft InfoPath с помощью Visual Studio 2012. Чтобы добавить обработчик событий в шаблон формы, сначала откройте шаблон формы в конструкторе InfoPath, а затем выберите соответствующую команду пользовательского интерфейса для события, для которого необходимо создать код. После выбора команды для события в конструкторе InfoPath фокус автоматически переключается на каркас обработчика событий для этого события в редакторе кода Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427187"
---
# <a name="add-an-event-handler"></a>Добавление обработчика событий

В этом разделе описываются процедуры добавления обработчиков событий в шаблон формы с управляемым кодом Microsoft InfoPath с помощью Visual Studio 2012. Чтобы добавить обработчик событий в шаблон формы, сначала откройте шаблон формы в конструкторе InfoPath, а затем выберите соответствующую команду пользовательского интерфейса для события, для которого необходимо создать код. После выбора команды для события в конструкторе InfoPath фокус автоматически переключается на каркас обработчика событий для этого события в редакторе кода Visual Studio 2012.
  
> [!IMPORTANT]
> Для добавления обработчика событий следует всегда использовать пользовательский интерфейс конструктора InfoPath. Добавление обработчика событий с помощью пользовательского интерфейса приводит к созданию кода привязки события в методе **InternalStartup** файла FormCode.cs или FormCode.vb в проекте шаблона формы. Не следует самостоятельно создавать метод **InternalStartup** или добавлять какой-либо дополнительный код. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Добавление обработчика событий Click для элемента управления "Кнопка"

1. Откройте шаблон формы в конструкторе InfoPath и добавьте в форму элемент управления **"Кнопка"** . 
    
2. Нажмите кнопку, а затем на вкладке **Свойства** ленты выберите **Пользовательский код**.
    
    Фокус переключается на каркас обработчика событий для события [clickd](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Добавление обработчика событий Changing, Validating и Changed для поля или группы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Щелкните правой кнопкой мыши элемент управления ввода данных, связанный с полем или группой, например элемент управления **Текстовое поле**. 
    
3. Щелкните **Программирование** и выберите событие, для которого необходимо создать обработчик. Фокус переключится на каркас обработчика событий для события [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) [Changed, Changed или Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) в редакторе кода Visual Studio 2012. [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) 
    
    > [!NOTE]
    > Команда для создания обработчика событий для события **Changing** не будет доступна, если параметр совместимости шаблона формы имеет значение **Форма веб-браузера**. Это связано с тем, что событие **Changing** не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 с помощью InfoPath Forms Services. Чтобы создать обработчик события для события **Changing**, необходимо в конструкторе InfoPath изменить параметр совместимости на **Форма редактора InfoPath**. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Добавление обработчика событий Loading, ViewSwitched, ContextChanged и Sign для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. На вкладке **Разработчик** ленты выберите событие формы, для которого требуется написать обработчик событий. 
    
    Фокус переключается на каркас обработчика событий для события [Load](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Команды для создания обработчика событий для событий [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) и [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) недоступны, если для шаблона формы задано значение " **Форма веб-браузера**". Это связано с тем, что эти события не поддерживаются в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 с помощью InfoPath Forms Services. Чтобы создать обработчик событий для события [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) , необходимо изменить параметр Совместимость на **форму редактора InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Добавление обработчика событий Submit для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **файл** , нажмите кнопку **передать** на вкладку **сведения** , а затем выберите команду * * Параметры передачи * *.
    
3. Последовательно щелкните **Разрешить пользователям отправлять эту форму**, **Выполнить пользовательское действие с использованием кода** и **Редактировать код**.
    
    Фокус переключается на каркас обработчика событий для события " [послать](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) " в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Добавление обработчика событий Save для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Сохранение**, установите флажок **Сохранить с использованием пользовательского кода**, а затем щелкните **Изменить**.
    
    Фокус переключается на каркас обработчика событий для события [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Флажок **Сохранить с использованием пользовательского кода** недоступен, если параметр совместимости шаблона формы имеет значение **Службы форм InfoPath**. Это связано с тем, что событие [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 с помощью InfoPath Forms Services. Чтобы создать обработчик событий для события [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) , необходимо изменить параметр Совместимость на **форму редактора InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Добавление обработчика событий VersionUpgrade для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Управление версиями**, выберите вариант **Использовать специальное событие** в раскрывающемся списке **Обновить существующие формы**, а затем щелкните **Изменить**.
    
    Фокус переключается на каркас обработчика событий для события [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Добавление обработчика событий Merge для формы

1. Откройте шаблон формы в конструкторе InfoPath.
    
2. Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Дополнительно**, установите флажки **Разрешить объединение форм** и **Объединить с использованием пользовательского кода**, а затем щелкните **Изменить**.
    
    Фокус переключится на каркас обработчика событий для события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Флажок **Разрешить объединение форм** недоступен, если для шаблона формы задано значение "свойства совместимости **InfoPath Forms Services**". Это связано с тем, что событие [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) не поддерживается в бизнес-логике шаблонов форм, опубликованных в библиотеках документов Microsoft SharePoint Server 2010 с помощью InfoPath Forms Services. Чтобы создать обработчик событий для события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , необходимо изменить параметр Совместимость на **форму редактора InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **Файл**, щелкните **Параметры форм**, **Совместимость** и установите **Тип формы****Форма редактора InfoPath**. 
  
## <a name="see-also"></a>См. также



[Пошаговое руководство: создание базового шаблона формы с кодом](walkthrough-creating-a-basic-form-template-with-code.md)

