---
title: Обработка событий форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Порядок событий [infopath 207], [InfoPath 2007], отвечать на запросы, порядок событий [InfoPath 2007] InfoPath 2007, реагирование на события, классы EventArgs [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Можно написать код, реагирующий на различные события, которые могут произойти при заполнении пользователем формы. Для работы с событиями в InfoPath следует добавить обработчики событий при работе с шаблоном формы в режиме конструктора.
ms.openlocfilehash: 7968837fe0ed524104111bc3f2960860af51c75a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807532"
---
# <a name="respond-to-form-events"></a>Обработка событий форм

Можно написать код, реагирующий на различные события, которые могут произойти при заполнении пользователем формы. Для работы с событиями в InfoPath следует добавить обработчики событий при работе с шаблоном формы в режиме конструктора.
  
Обработчики событий InfoPath необходимо всегда создавать в режиме конструктора, поскольку приложение InfoPath автоматически добавляет правильное описание для принятия события в метод **InternalStartup** и вставляет структуру кода обработчика событий в файл кода формы (FormCode.cs или FormCode.vb). После создания обработчика событий не следует изменять его объявление в файле кода формы. 
  
Сведения о создании обработчиков событий приложения InfoPath содержатся в разделе [Добавление обработчика событий](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Обзор классов событий

Модель InfoPath, предоставляемой пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) реализует три классы, реализующие 12 событий, которые вызвали и обрабатывается с помощью бизнес-логики шаблонов форм. В следующей таблице приведены каждого из объектов событий Microsoft InfoPath, события, связанные с ними и описание возможностей, предоставляемых. 
  
|**Имя**|**События**|**Описание**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Нажатии этой кнопки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |Класс **ButtonEvent** внедряет событие **Clicked**, вызываемое при щелчке элемента управления **Кнопка** в форме.   <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Загрузка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Объединение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Сохранение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Отправить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |Класс **FormEvents** внедряет события, специфичные для самого шаблона формы InfoPath:  <br/> **ContextChanged** <br/> Создается после изменения узла контекста.  <br/> **Загрузка** <br/> Создается после загрузки шаблона формы, но до инициализации какого-либо представления.  <br/> **Объединение** <br/> Происходит, когда команда **Объединить формы** вызывается из пользовательского интерфейса или работы InfoPath с `/aggregate` параметр командной строки.  <br/> **Сохранение** <br/> Происходит, когда используются команды **Сохранить** или **Сохранить как** из пользовательского интерфейса или при использовании [Сохранить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) и [Сохранить как](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) методы класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .  <br/> **Sign** <br/> Создается после того, как набор подписанных данных был выбран для подписи в диалоговом окне **Цифровые подписи**.  <br/> **Отправить** <br/> Происходит, когда используется команда **Отправить** из пользовательского интерфейса или используется метод [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) класса **XmlForm** .  <br/> **VersionUpgrade** <br/> Создается, если номер версии открываемой формы старше номера версии шаблона формы, на котором она основана.  <br/> **ViewSwitched** <br/> Создается после успешного переключения представления формы.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Изменен](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Изменение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Проверка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Внедряет события, порождаемые изменениями данных в базовом XML-документе экземпляра формы:  <br/> **Изменен** <br/> Возникает после принятия изменений в базовом XML-документе формы и после возникновения события **Validating**.  <br/> **Изменение** <br/> Создается после изменений в связанном XML-документе формы, но до принятия этих изменений.  <br/> **Проверка** <br/> Возникает после принятия изменений в базовом XML-документе формы, но до возникновения события **Changed**.  <br/> Класс **XmlEvent** также внедряет свойство [RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) , которое возвращает или задает вызов события **Changed** возникает при возникновении операции отмены или повтора действия.  <br/> |
   
> [!NOTE]
>  События **Changed** и **Changing** срабатывать только один раз при внесении изменений в поле непустых в форме, тогда как сравнимые события в InfoPath 2003 и объектной моделью совместимых с InfoPath 2003 предоставлено [ Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) пожарной пространства имен ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) и [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) дважды на изменения в поле непустых: один раз при удалении старое значение, и еще раз при вставке новое значение. 
  
## <a name="overview-of-the-eventargs-classes"></a>Обзор класса EventArgs

Каждое из 12 событий использует объект **EventArgs**, связанный с событием и передаваемый обработчику соответствующих событий для предоставления сведений о состоянии и других возможностей, которые можно использовать в коде обработчика событий. В следующей таблице перечисляются события InfoPath с соответствующими им объектами  **EventArgs** и краткие описания возможностей, предоставляемых свойствами и методами каждого объекта. Подробные сведения о конкретных свойствах и методах объектов можно вызвать, щелкнув имя объекта **EventArgs** в таблице, а затем щелкнув ссылку "Элементы" в теме. 
  
|**Событие**|**Класс EventsArgs**|**Описание**|
|:-----|:-----|:-----|
|**Нажатии этой кнопки** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Возвращает идентификатор элемента управления.  <br/> Возвращает объект **XPathNavigator**, располагающийся в наиболее вложенном XML-узле базового XML-документа формы, содержащего элемент управления **Кнопка**.  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Возвращает тип изменения контекста, выполняемого при возникновении события.   <br/> Возвращает значение, указывающее, возникает ли событие изменения контекста в ответ на операцию отмены или повтора действия.   <br/> Возвращает ссылку на объект **XPathNavigator**, расположенный в контекстном узле, породившем событие.   <br/> |
|**Загрузка** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Указывает представление, в котором будет открыта форма после загрузки.  <br/> Возвращает ссылку на объект **XmlFormCancelEventArgs**.  <br/> Возвращает объект **IDictionary** , содержащий любые входные параметры, заданные с помощью `/InputParameters` параметр командной строки или задается с помощью параметров в URL-АДРЕСЕ запроса, для открытия формы.  <br/> |
|**Объединение** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Возвращает ссылку на объект **XmlFormCancelEventArgs**.  <br/> Возвращает количество форм, объединенных в операции объединения.   <br/> Возвращает индекс объединяемой в данный момент формы (начиная с нуля).  <br/> Возвращает или задает значение, которое используется с свойством **Cancel** для определения выбора отмены только текущей формы или всей операции объединения.   <br/> Возвращает объект **XPathNavigator**, размещенный в корневом узле связанного XML-документа текущей объединяемой формы.  <br/> |
|**Сохранение** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Выполняет операцию сохранения, запрошенную пользователем.  <br/> Возвращает ссылку на объект **SaveCancelEventArgs**, который можно использовать для отмены события.  <br/> Возвращает имя файла для использования в обработчике событий применительно к данному событию.  <br/> Возвращает выбор для операции сохранения: "сохранить" или "сохранить как".   <br/> |
|**Sign** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Возвращает или задает факт отображения диалогового окна **Цифровые подписи**.   <br/> Возвращает набор подписываемых данных, порождаемых событием.  <br/> |
|**Отправить** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Возвращает ссылку на объект **XmlFormCancelEventArgs** для отмены события.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Возвращает ссылку на объект **XmlFormCancelEventArgs** для отмены события.  <br/> Возвращает номер версии обновляемого документа формы.  <br/> Возвращает номер версии шаблона формы, связанного с обновляемой формой.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |Класс **ViewSwitchedEventArgs** не предоставляет свойств и методов для событий, отличных от наследуемых из объекта **System.Object**.  <br/> |
|**Изменен** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Возвращает объект **XPathExpression**, содержащий выражение XPath, которое возвращает изменяемый в данный момент узел.   <br/> Возвращает новое значение изменяемого узла.   <br/> Возвращает объект **XPathNavigator**, указывающий на узел, являющийся родительским для удаляемого узла.   <br/> Возвращает исходное значение изменяемого узла.  <br/> Возвращает перечисление [XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) , указывающую тип операции, возникшей при изменении узла.  <br/> Возвращает объект **XPathNavigator**, указывающий на изменяемый узел.   <br/> Возвращает значение, указывающее, является ли изменяемый узел компонентом операции отмены или повтора действия.  <br/> |
|**Изменение** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Возвращает объект **XmlFormCancelEventArgs**, связанный с событием.   <br/> Наследует все возможности, перечисленные выше для объекта **XmlEventArgs**.  <br/> |
|**Проверка** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Создает объект [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) , который содержит сведения о настраиваемых ошибках с указанными значениями и добавляет его к объекту [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) формы.  <br/> Наследует все возможности, перечисленные выше для объекта **XmlEventArgs**.  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Использование объектов EventArgs

При создании обработчика событий приложение InfoPath создает объявление обработчика событий в коде формы проекта. В объявлении обработчика событий приложение InfoPath использует **e** в качестве имени параметра, передаваемого обработчику событий. Этот параметр содержит объект **EventArgs**, который связан с обработчиком событий и используется для предоставления сведений о состоянии и других возможностей при возникновении события.  
  
Например при создании обработчик событий для события **загрузки** в режиме конструктора (например, щелкнув меню **Для события загрузки** на вкладки " **Разработчик** ") InfoPath добавляет объявления для обработчика событий, который получает [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) Объект, который требуется файле кода формы, а затем открывает редактор кода, чтобы код можно добавить следующее объявление обработчика событий. 
  
```cs
public void FormEvents_Loading(object sender, LoadingEventArgs e)
{
   // Write your code here.
}
```

```vb
Public Sub FormEvents_Loading(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Write your code here.
End Sub
```

При написании кода для обработчика событий, можно использовать свойства и методы, объект **EventArgs** , передаваемых через параметр **e** . Например в следующий обработчик события **Changing** [новое значение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) свойства объекта [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) (который наследуется от класса [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) ) используется для проверки значения поля, который был только что изменен. Если пользователь изменил поле и оставить пустым, свойство [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) класса [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) осуществляется с помощью свойства [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) объекта **XmlChangingEventArgs** для отображения ошибки пользователю, и Свойство **XmlFormCancelEventArgs.Cancel** имеет значение **true**, чтобы отменить событие и откат изменений, внесенных пользователя.
  
```cs
public void field1_Changing(object sender, LoadingEventArgs e)
{
   // Determine whether there is a new value.
   if (e.NewValue == "")
   {
      // The value is blank, so display an error message
      // and roll back the changes.
      e.CancelableArgs.Message = 
         "You must supply a value for this field.";
      e.CancelableArgs.Cancel = true;
      return;
   }
}
```

```vb
Public Sub field1_Changing(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message 
      ' and roll back the changes.
      e.CancelableArgs.Message = _
         "You must supply a value for this field."
      e.CancelableArgs.Cancel = True
      Return
   End If
End Sub
```


