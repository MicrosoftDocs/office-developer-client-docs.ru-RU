---
title: Добавление обработчика событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- событие versionupgrade [infopath 2007], обработка событий [InfoPath 2007], изменение событий [InfoPath 2007], InfoPath 2007, добавление обработчиков событий, событие Changed [InfoPath 2007], событие ContextChanged [InfoPath 2007], нажмите кнопку события [InfoPath, событие [InfoPath 2007] Загрузка Добавление обработчиков событий, событие Sign [InfoPath 2007], событие ViewSwitched [InfoPath 2007], обработку событий [InfoPath 2007], событие Merge [InfoPath 2007], события Validating [InfoPath 2007], события Submit [InfoPath 2007], сохранить событий [InfoPath 2007] 2007] события [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: В этом разделе описываются процедуры для добавления обработчиков событий в шаблон формы управляемый код Microsoft InfoPath с помощью Visual Studio 2012. Чтобы добавить обработчик событий в шаблон формы, начать с шаблоном формы в конструкторе InfoPath откройте и выберите соответствующий пользовательский интерфейс команды для события, которого требуется написать код для объявления. После выбора команды для события в InfoPath Designer, фокус автоматически переключится на Структурный обработчик события для события в редакторе кода Visual Studio 2012.
ms.openlocfilehash: 5bac409fb859337b82bf6567dd4636e6d384ba59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807525"
---
# <a name="add-an-event-handler"></a>Добавление обработчика событий

В этом разделе описываются процедуры для добавления обработчиков событий в шаблон формы управляемый код Microsoft InfoPath с помощью Visual Studio 2012. Чтобы добавить обработчик событий в шаблон формы, начать с шаблоном формы в конструкторе InfoPath откройте и выберите соответствующий пользовательский интерфейс команды для события, которого требуется написать код для объявления. После выбора команды для события в InfoPath Designer, фокус автоматически переключится на Структурный обработчик события для события в редакторе кода Visual Studio 2012.
  
> [!IMPORTANT]
> Всегда следует использовать пользовательский интерфейс InfoPath Designer для добавления обработчика событий. Добавление обработчика событий с помощью интерфейса пользователя создает код привязки события в методе **InternalStartup** файле FormCode.cs или FormCode.vb в проект шаблона формы. Не следует создать метод **InternalStartup** или добавьте любые дополнительные код в ней самостоятельно. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Добавление обработчика событий Click для элемента управления "Кнопка"

1. Откройте шаблон формы в конструкторе InfoPath и добавьте в форму элемент управления **Button** . 
    
2. Нажмите кнопку и затем на вкладке **Свойства** ленты выберите **Пользовательский код**.
    
    Фокус переключится на Структурный обработчик события для события [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Добавление обработчика событий Changing, Validating и Changed для поля или группы

1. Откройте шаблон формы в InfoPath.
    
2. Щелкните правой кнопкой мыши элемент управления ввода данных, привязанных к поля или группы, такие как элемент управления **Текстовое поле** . 
    
3. Выберите пункт **программирование**и нажмите кнопку вы хотите создать обработчик событий для события. Фокус переключится на Структурный обработчик события для события [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) и [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Команду, чтобы создать обработчик событий для события **Changing** недоступен, если параметр совместимости для шаблона формы задано значение **Форма веб-браузера**. Это **событие** не поддерживается в бизнес-логике шаблоны форм следует публиковать в библиотеки документов на Microsoft SharePoint Server 2010 с помощью службы InfoPath Forms Services. Чтобы создать обработчик событий для события **Changing** , необходимо изменить значение параметра совместимости редактор **InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **файл** , нажмите кнопку **Параметры формы**, нажмите кнопку **совместимости**и установите для параметра **тип формы** в **Шаблон формы InfoPath**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Добавление обработчика событий Loading, ViewSwitched, ContextChanged и Sign для формы

1. Откройте шаблон формы в InfoPath.
    
2. На вкладке **Разработчик** ленты выберите событие формы, для которого требуется написать обработчик событий для. 
    
    Фокус переключится на Структурный обработчик события для события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [входа](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Команды, чтобы создать обработчик событий для события [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) и [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) недоступны, если параметр совместимости для шаблона формы задано значение **Форма веб-браузера**. Это, так как эти события не поддерживаются в бизнес-логике шаблоны форм следует публиковать в библиотеки документов на Microsoft SharePoint Server 2010 с помощью службы InfoPath Forms Services. Чтобы создать обработчик событий для события [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) или [входа](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) , необходимо изменить значение параметра совместимости **Шаблон формы InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **файл** , нажмите кнопку **Параметры формы**, нажмите кнопку **совместимости**и установите для параметра **тип формы** в **Шаблон формы InfoPath**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Добавление обработчика событий Submit для формы

1. Откройте шаблон формы в InfoPath.
    
2. Перейдите на вкладку **файл** , выберите пункт **Отправить** на вкладке **сведения** и нажмите кнопку ** Параметры отправки **.
    
3. Нажмите кнопку **Разрешить пользователям отправлять эту форму**, нажмите кнопку **выполнить пользовательское действие с использованием кода**и нажмите кнопку **Редактировать код**.
    
    Фокус переключится на Структурный обработчик события для события [отправки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Добавление обработчика событий Save для формы

1. Откройте шаблон формы в InfoPath.
    
2. Щелкните вкладку **Файл**, а затем  **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Сохранение** , установите флажок **Сохранить с использованием пользовательского кода** и нажмите кнопку **Изменить**.
    
    Фокус переключится на Структурный обработчик события для события [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Флажок **Сохранить с использованием пользовательского кода** недоступен, если параметр совместимости для шаблона формы **InfoPath Forms Services**. Это событие [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) не поддерживается в бизнес-логике шаблоны форм следует публиковать в библиотеки документов на Microsoft SharePoint Server 2010 с помощью службы InfoPath Forms Services. Чтобы создать обработчик событий для события [сохранения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) , необходимо изменить значение параметра совместимости **Шаблон формы InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **файл** , нажмите кнопку **Параметры формы**, нажмите кнопку **совместимости**и установите для параметра **тип формы** в **Шаблон формы InfoPath**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Добавление обработчика событий VersionUpgrade для формы

1. Откройте шаблон формы в InfoPath.
    
2. Щелкните вкладку **Файл**, а затем  **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Управление версиями** , выберите **использовать специальное событие** в раскрывающемся списке **Обновить существующие формы** и нажмите кнопку **Изменить**.
    
    Фокус переключится на Структурный обработчик события для события [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) в редакторе кода Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Добавление обработчика событий Merge для формы

1. Откройте шаблон формы в InfoPath.
    
2. Щелкните вкладку **Файл**, а затем  **Параметры формы** на вкладке **Сведения**. 
    
3. Выберите категорию **Дополнительно** , установите флажок **Разрешить объединение форм** , установите флажок **Объединить с использованием пользовательского кода** и нажмите кнопку **Изменить**.
    
    Фокус переключится на Структурный обработчик события для события [объединения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) в редакторе кода Visual Studio 2012. 
    
    > [!NOTE]
    > Флажок **Разрешить объединение форм** недоступен, если параметр совместимости для шаблона формы **InfoPath Forms Services**. Это событие [Объединение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) не поддерживается в бизнес-логике шаблоны форм следует публиковать в библиотеки документов на Microsoft SharePoint Server 2010 с помощью службы InfoPath Forms Services. Чтобы создать обработчик событий для события [объединения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , необходимо изменить значение параметра совместимости **Шаблон формы InfoPath** в конструкторе InfoPath. Для этого перейдите на вкладку **файл** , нажмите кнопку **Параметры формы**, нажмите кнопку **совместимости**и установите для параметра **тип формы** в **Шаблон формы InfoPath**. 
  
## <a name="see-also"></a>См. также



[Пошаговое руководство: Создание шаблона базовой формы с помощью кода](walkthrough-creating-a-basic-form-template-with-code.md)

