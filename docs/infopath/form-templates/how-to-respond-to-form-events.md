---
title: Реагирование на события формы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- порядок событий [infopath 207],events [InfoPath 2007], responding,events [InfoPath 2007], order,InfoPath 2007, reponding to events,EventArgs classes [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Можно написать код, реагирующий на различные события, которые могут произойти при заполнении пользователем формы. Для работы с событиями в InfoPath следует добавить обработчики событий при работе с шаблоном формы в режиме конструктора.
ms.openlocfilehash: 0db3209dfe005f2a87ad65f3fc89b1714ec7d95c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407685"
---
# <a name="respond-to-form-events"></a>Реагирование на события формы

Можно написать код, реагирующий на различные события, которые могут произойти при заполнении пользователем формы. Для работы с событиями в InfoPath следует добавить обработчики событий при работе с шаблоном формы в режиме конструктора.
  
Обработчики событий InfoPath необходимо всегда создавать в режиме конструктора, поскольку приложение InfoPath автоматически добавляет правильное описание для принятия события в метод **InternalStartup** и вставляет структуру кода обработчика событий в файл кода формы (FormCode.cs или FormCode.vb). После создания обработчика событий не следует изменять его объявление в файле кода формы. 
  
Дополнительные сведения о создании обработчиков событий InfoPath см. в [подстроке "Добавление обработчиков событий".](how-to-add-an-event-handler.md)
  
## <a name="overview-of-the-event-classes"></a>Обзор классов событий

Модель InfoPath, предоставляемая пространством имен [Microsoft.Office.InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) реализует три класса, реализуют 12 событий, которые могут быть и вызываются и обрабатываются бизнес-логикой шаблона формы. В следующей таблице перечисляются все объекты событий InfoPath, объекты, с которыми они связываются, а также описания предоставляемых ими возможностей. 
  
|**Название**|**События**|**Описание**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |Класс **ButtonEvent** внедряет событие **Clicked**, вызываемое при щелчке элемента управления **Кнопка** в форме.  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Загрузка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Отправить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |Класс **FormEvents** внедряет события, специфичные для самого шаблона формы InfoPath:  <br/> **ContextChanged** <br/> Создается после изменения узла контекста.  <br/> **Загрузка** <br/> Создается после загрузки шаблона формы, но до инициализации какого-либо представления.  <br/> **Merge** <br/> Возникает, когда команда **объединения форм** вызывается из пользовательского интерфейса или InfoPath начинается с коммутатора  `/aggregate` командной строки.  <br/> **Save** <br/> Возникает, когда команды  **"Сохранить** или сохранить как" используются из пользовательского интерфейса или когда используются методы [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) и [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)  <br/> **Sign** <br/> Создается после того, как набор подписанных данных был выбран для подписи в диалоговом окне **Цифровые подписи**.  <br/> **Отправить** <br/> Возникает, когда команда **Отправка** используется из пользовательского интерфейса или используется метод [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) класса **XmlForm.**  <br/> **VersionUpgrade** <br/> Создается, если номер версии открываемой формы старше номера версии шаблона формы, на котором она основана.  <br/> **ViewSwitched** <br/> Создается после успешного переключения представления формы.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Изменение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Изменение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Проверка](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Внедряет события, порождаемые изменениями данных в базовом XML-документе экземпляра формы:  <br/> **Изменение** <br/> Возникает после принятия изменений в базовом XML-документе формы и после возникновения события **Validating**.  <br/> **Изменение** <br/> Создается после изменений в связанном XML-документе формы, но до принятия этих изменений.  <br/> **Проверка** <br/> Возникает после принятия изменений в базовом XML-документе формы, но до возникновения события **Changed**.  <br/> Класс **XmlEvent** также реализует свойство [RaiseUndoRedoForChanged,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) которое возвращает или задает, будет ли событие **Changed** возникать при выполнении операции отмены или повторного выполнения.  <br/> |
   
> [!NOTE]
>  События **"Изменено"** и **"Изменение"** происходят только один раз при изменении непустого поля в форме. в то время как сравнимые события в InfoPath 2003 и объектной модели, совместимой с InfoPath 2003, предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) и [OnAfterChange),](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) дважды активировать при изменениях в непустом поле: один раз при удалении старого значения и еще раз при вставке нового значения. 
  
## <a name="overview-of-the-eventargs-classes"></a>Обзор класса EventArgs

Каждое из 12 событий использует объект **EventArgs**, связанный с событием и передаваемый обработчику соответствующих событий для предоставления сведений о состоянии и других возможностей, которые можно использовать в коде обработчика событий. В следующей таблице перечисляются события InfoPath с соответствующими им объектами  **EventArgs** и краткие описания возможностей, предоставляемых свойствами и методами каждого объекта. Подробные сведения о конкретных свойствах и методах объектов можно вызвать, щелкнув имя объекта **EventArgs** в таблице, а затем щелкнув ссылку "Элементы" в теме. 
  
|**Событие**|**Класс EventsArgs**|**Описание**|
|:-----|:-----|:-----|
|**Clicked** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Возвращает идентификатор элемента управления.  <br/> Возвращает объект **XPathNavigator**, располагающийся в наиболее вложенном XML-узле базового XML-документа формы, содержащего элемент управления **Кнопка**.  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Возвращает тип изменения контекста, выполняемого при возникновении события.  <br/> Возвращает значение, указывающее, возникает ли событие изменения контекста в ответ на операцию отмены или повтора действия.   <br/> Возвращает ссылку на объект **XPathNavigator**, расположенный в контекстном узле, породившем событие.   <br/> |
|**Загрузка** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Указывает представление, в котором будет открыта форма после загрузки.  <br/> Возвращает ссылку на объект **XmlFormCancelEventArgs**.  <br/> Получает **IDictionary,** содержащий любые входные параметры, указанные с помощью параметра командной строки или указанные с помощью параметров запроса в URL-адресе для  `/InputParameters` открытия формы.  <br/> |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Возвращает ссылку на объект **XmlFormCancelEventArgs**.  <br/> Возвращает количество форм, объединенных в операции объединения.  <br/> Возвращает индекс объединяемой в данный момент формы (начиная с нуля).  <br/> Возвращает или задает значение, которое используется с свойством **Cancel** для определения выбора отмены только текущей формы или всей операции объединения.   <br/> Возвращает объект **XPathNavigator**, размещенный в корневом узле связанного XML-документа текущей объединяемой формы.  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Выполняет операцию сохранения, запрошенную пользователем.  <br/> Возвращает ссылку на объект **SaveCancelEventArgs**, который можно использовать для отмены события.  <br/> Возвращает имя файла для использования в обработчике событий применительно к данному событию.  <br/> Возвращает выбор для операции сохранения: "сохранить" или "сохранить как".   <br/> |
|**Sign** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Возвращает или задает факт отображения диалогового окна **Цифровые подписи**.  <br/> Возвращает набор подписываемых данных, порождаемых событием.  <br/> |
|**Отправить** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Возвращает ссылку на объект **XmlFormCancelEventArgs** для отмены события.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Возвращает ссылку на объект **XmlFormCancelEventArgs** для отмены события.  <br/> Возвращает номер версии обновляемого документа формы.  <br/> Возвращает номер версии шаблона формы, связанного с обновляемой формой.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |Класс **ViewSwitchedEventArgs** не предоставляет свойств и методов для событий, отличных от наследуемых из объекта **System.Object**.  <br/> |
|**Изменение** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Возвращает объект **XPathExpression**, содержащий выражение XPath, которое возвращает изменяемый в данный момент узел.  <br/> Возвращает новое значение для изменяемого узла.  <br/> Возвращает объект **XPathNavigator**, указывающий на узел, являющийся родительским для удаляемого узла.  <br/> Возвращает начальное значение изменяемого узла.  <br/> Получает [enumeration XmlOperation,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) которое указывает тип операции, которая произошла при смене узла.  <br/> Возвращает объект **XPathNavigator**, указывающий на изменяемый узел.  <br/> Возвращает значение, которое указывает, является ли изменяемый узел частью операции отмены или возращения.  <br/> |
|**Изменение** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Возвращает объект **XmlFormCancelEventArgs**, связанный с событием.  <br/> Наследует все возможности, перечисленные выше для объекта **XmlEventArgs**.  <br/> |
|**Проверка** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Создает объект [FormError,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) содержащий пользовательские сведения об ошибке с указанными значениями, и добавляет его в объект [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) формы.  <br/> Наследует все возможности, перечисленные выше для объекта **XmlEventArgs**.  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Использование объектов EventArgs

При создании обработчика событий приложение InfoPath создает объявление обработчика событий в коде формы проекта. В объявлении обработчика событий приложение InfoPath использует **e** в качестве имени параметра, передаваемого обработчику событий. Этот параметр содержит объект **EventArgs**, который связан с обработчиком событий и используется для предоставления сведений о состоянии и других возможностей при возникновении события. 
  
Например, когда вы создаете обработчик события  **Loading** в режиме конструктора (щелкнув меню "Событие загрузки" на вкладке "Разработчик"), InfoPath добавляет объявление обработчик событий, который получает объект  [LoadingEventArgs,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) в файл кода формы, а затем открывает редактор кода, чтобы можно было добавить код в следующее объявление обработчика событий. 
  
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

При написании кода для обработчика событий можно использовать свойства и методы, реализуемые объектом **EventArgs**, который передается через параметр **e**. Например, в следующем обработчивом событии **Changing** свойство [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) объекта [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) (наследуется от класса [XmlEventArgs)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) используется для проверки значения только что измененного поля. Если пользователь изменил поле и оставил его пустым, доступ к свойству [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) класса [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) можно получить с помощью свойства [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) объекта **XmlChangingEventArgs,** чтобы отобразить ошибку для пользователя, а для свойства **XmlFormCancelEventArgs.Cancel** установлено **true,** чтобы отменить событие и откатить изменения, внесенные пользователем.
  
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


