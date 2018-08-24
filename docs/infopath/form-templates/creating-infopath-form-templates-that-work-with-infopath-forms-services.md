---
title: Создание шаблонов форм InfoPath, работающих со службами InfoPath Forms Services
manager: soliver
ms.date: 03/20/2015
ms.audience: Developer
keywords:
- browser-compatible form templates [infopath 2007],forms [InfoPath 2007], browser-compatible,browser-compatible forms [InfoPath 2007],form templates [InfoPath 2007], browser-compatible,InfoPath 2007, browser-compatible forms,business logic, InfoPath Forms Services,InfoPath Forms Services, creating forms,InfoPath Forms Services, supported object model members,InfoPath Forms Services, supported classes and members
localization_priority: Normal
ms.assetid: 7bd4fbbb-49c6-46a1-9584-895e5aa9a772
description: Формы с поддержкой веб-браузера развернут в Microsoft SharePoint Server 2013 с помощью возможности поддержки службы InfoPath Forms Services и элементов управления, которые охватывают в большинстве случаев использования форм InfoPath. Однако формы с поддержкой веб-браузера, предоставляемые InfoPath Forms Services, поддерживают не все функции InfoPath. Некоторые функции и элементы управления не реализованы на сервере. Другие функции не имеют адекватного представления на сервере.
ms.openlocfilehash: c633c93eef5fa2d773ed1497f933f2cc3ee0e3bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595456"
---
# <a name="creating-infopath-form-templates-that-work-with-infopath-forms-services"></a>Создание шаблонов форм InfoPath, работающих со службами InfoPath Forms Services

Формы с поддержкой веб-браузера развернут в Microsoft SharePoint Server 2013 с помощью возможности поддержки службы InfoPath Forms Services и элементов управления, которые охватывают в большинстве случаев использования форм InfoPath. Однако формы с поддержкой веб-браузера, предоставляемые InfoPath Forms Services, поддерживают не все функции InfoPath. Некоторые функции и элементы управления не реализованы на сервере. Другие функции не имеют адекватного представления на сервере.
  
В следующих разделах указано, какие функции поддерживаются в формах с поддержкой веб-браузера, какие функции нельзя использовать в таких формах, а какие функции можно указать для форм с поддержкой веб-браузера, но работать в веб-браузере они не будут.
  
## <a name="features-supported-by-both-infopath-and-infopath-forms-services"></a>Функции, поддерживаемые и в приложении InfoPath, и в службах InfoPath Forms Services

В следующих разделах перечислены функции, которые поддерживаются шаблонами форм с поддержкой веб-браузера, развернутыми в InfoPath Forms Services и доступными для открытия как в InfoPath, так и в веб-браузере.
  
### <a name="controls"></a>Элементы управления

Следующие элементы управления поддерживаются в шаблонах форм, которые могут быть открыты только в InfoPath и веб-браузере.
  
- **Текстовое поле**
    
- **Форматированный текст** (доступно для редактирования только в Microsoft Internet Explorer) 
    
- **Раскрывающийся список**
    
- **Список**
    
- **Выбор даты** (в веб-браузерах, отличных от Internet Explorer, обрабатывается как текстовое поле) 
    
- **Флажок**
    
- **Переключатель**
    
- **Кнопка**
    
- **Раздел**
    
- **Дополнительный раздел**
    
- **Повторяющийся раздел**
    
- **Повторяющаяся таблица**
    
- **Вложенный файл**
    
- **Гиперссылка**
    
- **Поле выражения**
    
- **Поле со списком**
    
- **Выбор нескольких строк списка**
    
- **Маркированный список**
    
- **Нумерованный список**
    
- **Простой список**
    
- **Рисунок**
    
- **Группа выбора**
    
- **Раздел выбора**
    
- **Средство выбора людей и групп**
    
- **Средство выбора внешних элементов**
    
- **Рисунок кнопки**
    
- **Рассчитанные преимущества**
    
### <a name="declarative-features"></a>Описательные функции

Прочие описательные функции, работающие как в InfoPath, так и в веб-браузере:
  
- Правила
    
- Вычисления
    
- Проверка
    
> [!NOTE]
> [!Примечание] Простые правила, расчеты и утверждения данных разрешены и запускаются через веб-браузер с использованием JScript. Сложные правила, расчеты и утверждения данных требуют обратной передачи для выполнения этих операций на сервере. 
  
### <a name="code"></a>Программа

Код бизнес-логики должен основываться на объектной модели InfoPath с управляемым кодом, предоставляемой пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . На запускаемый на сервере код бизнес-логики накладываются следующие ограничения: 
  
- Поскольку разные серверные запросы могут обрабатываться разными интерфейсными серверами, а также в связи с тем, что InfoPath Forms Services может загружать только один экземпляр бизнес-логики, программистам нельзя полагаться на данные, хранящиеся в глобальных или статических переменных. Чтобы устранить эту проблему, бизнес-логика должна сохранять состояние в контейнер свойств, доступ к которому предоставляется свойством [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) . 
    
- Подмножество элементов пространства имен **Microsoft.Office.InfoPath** предоставляет ряд функций, таких как управление правами на доступ к данным (IRM), которые не поддерживаются на сервере. Дополнительные сведения о том, какие элементы объектной модели поддерживаются, а какие нет, см. в разделах "Элементы объектной модели, работающие в приложении InfoPath и в службах InfoPath Forms Services" и "Элементы объектной модели, работающие только в приложении InfoPath" далее в этой теме. 
    
- Бизнес-логика, написанная с помощью VBScript, JScript и объектной модели, совместимой с InfoPath 2003, которая предоставляется пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , на сервере не поддерживается. 
    
## <a name="features-not-supported-by-infopath-forms-services"></a>Функции, не поддерживаемые службами InfoPath Forms Services

В следующих разделах перечисляются функции, которые не поддерживаются шаблонами форм с поддержкой веб-браузера, развернутыми в InfoPath Forms Services и доступными для открытия как в InfoPath, так и в веб-браузере.
  
При использовании функции **Проверка макета** в режиме конструктора InfoPath для подтверждения совместимости с InfoPath Forms Services неподдерживаемые функции будут приводить к выводу ошибок либо сообщений. Функции, вызывающие ошибки, не позволят публиковать шаблон формы в качестве формы с поддержкой веб-браузера. Функции, приводящие к выводу сообщений, допустимы, но при открытии формы в веб-браузере эти функции не будут запускаться. 
  
### <a name="controls"></a>Элементы управления

Следующие элементы управления и функции элементов управления не поддерживаются в шаблонах форм, доступных для открытия как в InfoPath, так и в веб-браузере:
  
- Фильтр повторяющихся элементов управления
    
- **Основной/подробности**
    
- **Вертикальная надпись**
    
- **Горизонтальная повторяющаяся таблица**
    
- **Рисунок от руки**
    
- **Повторяющийся рекурсивный раздел**
    
### <a name="other-features-that-are-not-supported-or-not-fully-supported-by-infopath-forms-services"></a>Прочие функции, которые не поддерживаются или не полностью поддерживаются службами InfoPath Forms Services

Другие функции, которые не поддерживаются в InfoPath Forms Services:
  
- Элементы управления ActiveX
    
- Области задач HTML
    
- Замещающий текст в элементах управления. Например, "Введите текст" (в веб-браузере этот текст не отображается)
    
- Подключения к данным баз данных ограничены доступом только для чтения к базам данных сервера SQL
    
- Роли пользователей
    
- Расширяемость цифровых подписей посредством объектной модели. Цифровые подписи на сервере поддерживаются посредством элемента управления ActiveX, который запускается только в веб-браузере Microsoft Internet Explorer.
    
- Интеграция службы HWS. Служба HWS не рекомендуется сервером BizTalk
    
- Переопределения сообщения об ошибке схемы XML. Эта редко используемая функция позволяет разработчику формы предоставить сообщение, отличное от предоставляемого службой MSXML или **System.Xml**, когда документ не проходит проверку (как правило, в связи с несовпадением типов). Эта функция не поддерживается в пользовательском интерфейсе конструктора и требует ручного редактирования файла определения формы (XSF). 
    
### <a name="features-with-no-direct-parallel-on-the-infopath-forms-services"></a>Функции, не имеющие прямых аналогов в службах InfoPath Forms Services

Другие возможности, которые не поддерживаются в InfoPath Forms Services:
  
- Всплывающие диалоговые окна при немодальной проверке
    
- Интеграция с Outlook
    
- Надстройки COM
    
- Объединение форм
    
- Автосохранение, обнаружение сбоев и восстановление после сбоев
    
- Почтовый конверт
    
- Экспорт в Excel
    
- Функции планшета и рукописного ввода, включая элемент управления **Рисунок от руки** 
    
- Отменить или повторить
    
- Управление правами на доступ к данным.
    
- Модальные диалоговые окна из бизнес-логики
    
- Расширяемость XSLT (блоки **xd:preserve**) 
    
- Внешняя автоматизация
    
- Автономное кэширование запросов
    
- Проверка правописания
    
- Режим безопасности "Ограниченный"
    
> [!NOTE]
> [!Примечание] Эти функции не приводят к ошибкам или уведомлениям при использовании функции **Проверка макета** в режиме конструктора InfoPath. 
  
## <a name="object-model-members-that-work-in-both-infopath-and-infopath-forms-services"></a>Элементы объектной модели, работающие как в приложении InfoPath, так и в службах InfoPath Forms Services

Приложение InfoPath предоставляет новую объектную модель с управляемым кодом, использующую базовый набор возможностей для создания настраиваемой бизнес-логики в шаблонах форм. При развертывании в SharePoint Server 2010 с InfoPath Forms Services бизнес-логика, созданная с помощью новой объектной модели, будет запускаться как в веб-браузере, так и в InfoPath. При необходимости можно написать бизнес-логику, использующую дополнительные возможности объектной модели, которые будут запускаться только в шаблонах форм, открытых для редактирования в InfoPath.
  
Чтобы написать бизнес-логику, которая будет запускаться при открытии формы как в веб-браузере, так и в InfoPath, установите флажок **Включить только возможности, совместимые с веб-браузером** в диалоговом окне **Создание шаблона формы** при создании нового шаблона формы. Чтобы написать бизнес-логику, которая будет использовать дополнительные возможности только при открытии в InfoPath, снимите флажок **Включить только возможности, совместимые с веб-браузером** при создании нового шаблона формы. Также можно изменить этот параметр после создания шаблона формы, щелкнув **Изменить параметры совместимости** в области задач **Проверка макета**, а затем установив или сняв флажок **Макет шаблона формы, который можно открыть в веб-браузере или в InfoPath**. Если требуется создать шаблон формы с поддержкой веб-браузера, то компилятор отобразит ошибку в случае использования любых классов или элементов, несовместимых с InfoPath Forms Services. 
  
> [!NOTE]
> [!Примечание] После публикации шаблона формы с поддержкой веб-браузера и наличием управляемого кода в SharePoint Server 2010 с InfoPath Forms Services или в общую папку необходимо отправить шаблон формы администратору сервера и получить его одобрение, чтобы шаблон можно было запускать. 
  
Следующие классы и элементы объектной модели InfoPath с управляемым кодом, предоставляемые пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , поддерживаются как в InfoPath, так и в InfoPath Forms Services. 
  
|**Родительский класс**|**Участники**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Команда](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Command.aspx) <br/> |
||[Подключение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Timeout.aspx) <br/> |
||[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Команда](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Command.aspx) <br/> |
||[Подключение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Timeout.aspx) <br/> |
|[Приложение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[Среда](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) <br/> |
||[Имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) <br/> |
||[user](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.User.aspx) <br/> |
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Нажатии этой кнопки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[ControlId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.ControlId.aspx) <br/> |
||[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) <br/> |
|[События элемента управления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.aspx) <br/> |[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.Item.aspx) <br/> |
|[Подключение данных](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) <br/> |[Выполнение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) <br/> |
||[Имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Name.aspx) <br/> |
|[DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) <br/> |
||[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) <br/> |
||[Имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx) <br/> |
||[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) <br/> |
||[Только для чтения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) <br/> |
||[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) <br/> |
|[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
|[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.aspx) <br/> |[None](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.None.aspx) <br/> |
||[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.Xml.aspx) <br/> |
||[XmlXsn](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.XmlXsn.aspx) <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[AttachmentFileName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.AttachmentFileName.aspx) <br/> |
||[Скрытой копии](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Bcc.aspx) <br/> |
||[«КОПИЯ»](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.EmailAttachmentType.aspx) <br/> |
||[Выполнение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) <br/> |
||[Введение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Introduction.aspx) <br/> |
||[Subject](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Subject.aspx) <br/> |
||[Задача](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.To.aspx) <br/> |
|[Среда](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) <br/> |[IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) <br/> |
||[IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) <br/> |
|[EventManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.aspx) <br/> |[События элемента управления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.ControlEvents.aspx) <br/> |
||[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.FormEvents.aspx) <br/> |
||[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.XmlEvents.aspx) <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Выполнение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) <br/> |
||[Filelocation, который](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.FileLocation.aspx) <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Выполнение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) <br/> |
||[Имя файла](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Filename.aspx) <br/> |
||[FolderUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.FolderUrl.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) <br/> |
||[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) <br/> |
||[Сообщение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) <br/> |
||[Имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Name.aspx) <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx) <br/> |
||[удаление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx); <br/> |
||[удаление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx); <br/> |
||[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetEnumerator.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx) <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.aspx) <br/> |[SchemaValidation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SchemaValidation.aspx) <br/> |
||[SystemGenerated](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SystemGenerated.aspx) <br/> |
||[UserDefined](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.UserDefined.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[Загрузка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> |
||[Отправить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> |
||[VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> |
||[ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) <br/> |
||[OpenFileFromPackage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.OpenFileFromPackage.aspx) <br/> |
||[URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) <br/> |
||[Версия](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) <br/> |
|[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.CancelableArgs.aspx) <br/> |
||[InputParameters](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.InputParameters.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Выполнение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) <br/> |
||[QueryThisFormOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.QueryThisFormOnly.aspx) <br/> |
||[SiteUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.SiteUrl.aspx) <br/> |
|[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.CancelableArgs.aspx) <br/> |
|[user](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[LoginName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.LoginName.aspx) <br/> |
||[Имя пользователя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) <br/> |
|[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.CancelableArgs.aspx) <br/> |
||[DocumentVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.DocumentVersion.aspx) <br/> |
||[FormTemplateVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.FormTemplateVersion.aspx) <br/> |
|[Просмотр](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Caption.aspx) <br/> |
||[Имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Name.aspx) <br/> |
|[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Count.aspx) <br/> |
||[Значение по умолчанию](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Default.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.GetEnumerator.aspx) <br/> |
||[Начальное](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Выполнение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) <br/> |
||[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) <br/> |
||[ServiceUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.ServiceUrl.aspx) <br/> |
||[SoapAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.SoapAction.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Timeout.aspx) <br/> |
||[WsdlUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.WsdlUrl.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Изменен](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> |
||[RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) <br/> |
||[Проверка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[Соответствие](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Match.aspx) <br/> |
||[Новое значение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) <br/> |
||[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) <br/> |
||[OldValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldValue.aspx) <br/> |
||[Операция](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Operation.aspx) <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) <br/> |
||[UndoRedo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.UndoRedo.aspx) <br/> |
|[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.aspx) <br/> |[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) <br/> |
||[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) <br/> |
||[Источники данных](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) <br/> |
||[сведения об ошибках](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx); <br/> |
||[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) <br/> |
||[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) <br/> |
||[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) <br/> |
||[Новый](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) <br/> |
||[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) <br/> |
||[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) <br/> |
||[Только для чтения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) <br/> |
||[Подпись](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) <br/> |
||[Отправить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) <br/> |
||[шаблон](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx). <br/> |
||[URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx) <br/> |
||[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) <br/> |
||[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) <br/> |
|[XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) <br/> |[Сообщение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) <br/> |
||[MessageDetails](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.MessageDetails.aspx) <br/> |
|[XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) <br/> |[удаление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Delete.aspx); <br/> |
||[Вставка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Insert.aspx) <br/> |
||[None](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.None.aspx) <br/> |
||[ValueChange](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.ValueChange.aspx) <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
|[XPathTypedValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.aspx) <br/> |[Оценка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.Evaluate.aspx) <br/> |
||[SetStringValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.SetStringValue.aspx) <br/> |
||[ToString](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.ToString.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.XPath.aspx) <br/> |
   
## <a name="object-model-members-that-work-only-in-infopath"></a>Элементы объектной модели, работающие только в приложении InfoPath

Следующие классы и элементы объектной модели InfoPath с управляемым кодом, предоставляемые пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , поддерживаются только в InfoPath. 
  
> [!NOTE]
> Эти элементы объектной модели можно использовать в коде шаблона формы с поддержкой веб-браузера, если записать условную логику, которая определяет, является ли форма открывается в браузере или в InfoPath. Дополнительные сведения можно [записать условной логики, определяет среды выполнения](how-to-write-conditional-logic-that-determines-the-run-time-environment.md). 
  
|**Родительский класс**|**Участники**|
|:-----|:-----|
|[Тип действия](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.aspx) <br/> |[Copy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Copy.aspx) <br/> |
||[Вырезание](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Cut.aspx) <br/> |
||[удаление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Delete.aspx); <br/> |
||[Вставить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Paste.aspx) <br/> |
||[XCollectionInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsert.aspx) <br/> |
||[XCollectionInsertAfter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertAfter.aspx) <br/> |
||[XCollectionInsertBefore](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertBefore.aspx) <br/> |
||[XCollectionRefreshFilter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRefreshFilter.aspx) <br/> |
||[XCollectionRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemove.aspx) <br/> |
||[XCollectionRemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemoveAll.aspx) <br/> |
||[XFileAttachmentAttach](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentAttach.aspx) <br/> |
||[XFileAttachmentOpen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentOpen.aspx) <br/> |
||[XFileAttachmentRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentRemove.aspx) <br/> |
||[XFileAttachmentSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentSaveAs.aspx) <br/> |
||[XOptionalInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalInsert.aspx) <br/> |
||[XOptionalRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalRemove.aspx) <br/> |
||[XReplaceReplace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XReplaceReplace.aspx) <br/> |
|[Приложение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) <br/> |
||[CacheFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.CacheFormTemplate.aspx) <br/> |
||[ComAddIns](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ComAddIns.aspx) <br/> |
||[GetFormTemplateLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.GetFormTemplateLocation.aspx) <br/> |
||[IsDestinationReachable](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.IsDestinationReachable.aspx) <br/> |
||[LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) <br/> |
||[MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) <br/> |
||[Завершите работу](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[Завершите работу](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[UnregisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UnregisterFormTemplate.aspx) <br/> |
||[UsableHeight](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableHeight.aspx) <br/> |
||[UsableWidth](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableWidth.aspx) <br/> |
||[Версия](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) <br/> |
||["Windows";](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) <br/> |
||[XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) <br/> |
|[Сертификат](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.ExpirationDate.aspx) <br/> |
||[IssuedBy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedBy.aspx) <br/> |
||[IssuedTo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedTo.aspx) <br/> |
||[Состояние](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.Status.aspx) <br/> |
|[CertificateStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.aspx) <br/> |[Ошибка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Error.aspx) <br/> |
||[Истек срок действия](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Expired.aspx) <br/> |
||[NotTrusted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.NotTrusted.aspx) <br/> |
||[Отменено](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Revoked.aspx) <br/> |
||[Допустимый](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Valid.aspx) <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Метод ChangeType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.ChangeType.aspx) <br/> |
||[Контекст](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) <br/> |
||[UndoRedo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.UndoRedo.aspx) <br/> |
|[ErrorMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.aspx) <br/> |[Модальные окна](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modal.aspx) <br/> |
||[MODELESS](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modeless.aspx) <br/> |
|[ExportFormat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.aspx) <br/> |[MHT](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Mht.aspx) <br/> |
||[Pdf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Pdf.aspx) <br/> |
||[XPS](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Xps.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> |
||[Объединение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> |
||[Сохранение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) <br/> |
|[HtmlTaskPane](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.aspx) <br/> |[HtmlDocument](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlDocument.aspx) <br/> |
||[HtmlWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlWindow.aspx) <br/> |
||[Переход](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.Navigate.aspx) <br/> |
|[MachineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.aspx) <br/> |[IEInOfflineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.IEInOfflineState.aspx) <br/> |
||[Автономный режим](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Offline.aspx) <br/> |
||[Оперативный режим](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Online.aspx) <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) <br/> |[Available](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Available.aspx) <br/> |
||[Скрытой копии](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Bcc.aspx) <br/> |
||[«КОПИЯ»](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.EmailAttachmentType.aspx) <br/> |
||[Введение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Introduction.aspx) <br/> |
||[Subject](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Subject.aspx) <br/> |
||[Задача](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.To.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Visible.aspx) <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.CancelableArgs.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Count.aspx) <br/> |
||[Индекс](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Index.aspx) <br/> |
||[Откат](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Rollback.aspx) <br/> |
||[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) <br/> |
|[Разрешение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) <br/> |[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) <br/> |
||[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) <br/> |
||[Включена](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) <br/> |
||[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) <br/> |
||[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) <br/> |
||[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) <br/> |
||[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) <br/> |
||[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) <br/> |
||[Разрешенияпользователя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) <br/> |
|[PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) <br/> |[Изменение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Change.aspx) <br/> |
||[Изменение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Edit.aspx) <br/> |
||[Извлечение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Extract.aspx) <br/> |
||[FullControl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.FullControl.aspx) <br/> |
||[ObjectModel](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.ObjectModel.aspx) <br/> |
||[Печать](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Print.aspx) <br/> |
||[Read](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Read.aspx) <br/> |
||[Сохранение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Save.aspx) <br/> |
||[Просмотр](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.View.aspx) <br/> |
|[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.CancelableArgs.aspx) <br/> |
||[CloseIfSaveCancelled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveCancelEventArgs.CloseIfSaveCancelled.aspx) <br/> |
||[Имя файла](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.Filename.aspx) <br/> |
||[IsSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.IsSaveAs.aspx) <br/> |
||[PerformSaveOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.PerformSaveOperation.aspx) <br/> |
|[Подпись](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[Сертификат](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Certificate.aspx) <br/> |
||[�����������](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Comment.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) <br/> |
||[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) <br/> |
||[Состояние](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Status.aspx) <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Count.aspx) <br/> |
||[CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Item.aspx) <br/> |
|[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.aspx) <br/> |[Скрепляющая](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Cosign.aspx) <br/> |
||[Скрепляющей](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.CounterSign.aspx) <br/> |
||[Single](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Single.aspx) <br/> |
|[SignatureStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.aspx) <br/> |[Ошибка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Error.aspx) <br/> |
||[Invalid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Invalid.aspx) <br/> |
||[Unsupported](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Unsupported.aspx) <br/> |
||[Допустимый](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Valid.aspx) <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Caption.aspx) <br/> |
||[Имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Name.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) <br/> |
||[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) <br/> |
||[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureRelation.aspx) <br/> |
||[Подписи](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.XPath.aspx) <br/> |
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Item.aspx) <br/> |
||[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.ShowSignatureDialog.aspx) <br/> |
|[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |
||[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |
|[Область задач](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.aspx) <br/> |[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.TaskPaneType.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.Visible.aspx) <br/> |
|[TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
|[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.aspx) <br/> |[BulletsNumbering](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.BulletsNumbering.aspx) <br/> |
||[Клипов](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ClipArt.aspx) <br/> |
||[Найти](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Find.aspx) <br/> |
||[форматирование;](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Formatting.aspx) <br/> |
||[HTML-код](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Html.aspx) <br/> |
||[ParagraphFormatting](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ParagraphFormatting.aspx) <br/> |
||[Заменить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Replace.aspx) <br/> |
||[Проверки орфографии](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Spelling.aspx) <br/> |
|[user](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[IsUserMemberOf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.IsUserMemberOf.aspx) <br/> |
|[UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) <br/> |[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) <br/> |
||[Разрешение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) <br/> |
||[Удаление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) <br/> |
||[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) <br/> |
|[UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Удаление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) <br/> |
||[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) <br/> |
|[Просмотр](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) <br/> |
||[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[Экспорт](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) <br/> |
||[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) <br/> |
||[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[HideName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.HideName.aspx) <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) <br/> |[Активация](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) <br/> |
||[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) <br/> |
||[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) <br/> |
||[Закрыть](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[Закрыть](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) <br/> |
||[Высота](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) <br/> |
||[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) <br/> |
||[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) <br/> |
||[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) <br/> |
||[Ширина](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) <br/> |
||[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) <br/> |
||[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) <br/> |
||[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) <br/> |
|[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx) <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) <br/> |[Развернуто](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Maximized.aspx) <br/> |
||[Свернуто](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Minimized.aspx) <br/> |
||[Normal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Normal.aspx) <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) <br/> |[Конструктор](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Designer.aspx) <br/> |
||[Редактор](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Editor.aspx) <br/> |
|[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Изменение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Закрыть](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx) <br/> |
||[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) <br/> |
||[Расширение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) <br/> |
||[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) <br/> |
||[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) <br/> |
||[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) <br/> |
||[Размещенные](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) <br/> |
||[Имя узла](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[Разрешение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) <br/> |
||[Печать](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Печать](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Восстановить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) <br/> |
||[Сохранение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) <br/> |
||[Сохранить как](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) <br/> |
||[SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) <br/> |
||[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) <br/> |
||[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) <br/> |
||[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.GetEnumerator.aspx) <br/> |
||[Элемент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx) <br/> |
||[Новый](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[Новый](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[Open](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
||[Open](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
|[XmlFormOpenMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormOpenMode.aspx) <br/> |**XmlFormOpenMode.Default** <br/> |
||**XmlFormOpenMode.FailOnVersionMismatch** <br/> |
||**XmlFormOpenMode.FailOnVersionOlder** <br/> |
||**XmlFormOpenMode.IgnoreDataConnectionsFailure** <br/> |
||**XmlFormOpenMode.PromptIfSigned** <br/> |
||**XmlFormOpenMode.ReadOnly** <br/> |
||**XmlFormOpenMode.TransformEvenIfSigned** <br/> |
||**XmlFormOpenMode.UseExistingVersion** <br/> |
||**XmlFormOpenMode.UseFileConverter** <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
   

