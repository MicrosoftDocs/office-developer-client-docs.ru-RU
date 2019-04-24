---
title: Реагирование на события формы с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны форм [InfoPath 2007], реагирование на события, шаблоны форм, совместимые с InfoPath 2003, реагирование на события формы
localization_priority: Normal
ms.assetid: 59e9c1ed-32a8-4bcd-bdfc-9aa568a34d2a
description: Можно написать код, реагирующий на различные события, которые могут происходить при заполнении пользователем формы. Для работы с событиями в InfoPath в режиме конструктора InfoPath создаются обработчики событий.
ms.openlocfilehash: b7347f882df991e64bdf4e76c471b1220a84dc58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300100"
---
# <a name="respond-to-form-events-using-the-infopath-2003-object-model"></a>Реагирование на события формы с помощью объектной модели InfoPath 2003

Можно написать код, реагирующий на различные события, которые могут происходить при заполнении пользователем формы. Для работы с событиями в InfoPath в режиме конструктора InfoPath создаются обработчики событий.
  
Обработчики событий InfoPath следует создавать в конструкторе InfoPath, так как при использовании объектной модели, совместимой с InfoPath 2003, InfoPath автоматически добавляет правильное объявление и применяет атрибут ([инфопасевенсандлераттрибуте](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) в файл кода формы (FormCode.cs или FormCode. vb) для идентификации и приема обработчика событий. После создания обработчика событий не следует менять его объявление и атрибут в файле кода формы. 
  
Сведения о создании обработчиков событий InfoPath приведены в статье [Добавление обработчика событий с помощью объектНой модели infopath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="overview-of-the-event-objects"></a>Обзор объектов событий

Объектная модель, совместимая с InfoPath 2003, реализует девять объектов Event, которые представлены в пространстве имен [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . В приведенной ниже таблице перечислены все объекты событий InfoPath, связанные с ними обработчики событий, а также приведено описание выполняемых ими функций. 
  
|**Name**|**обработчики событий;**|**Описание**|
|:-----|:-----|:-----|
|[DataDOMEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.aspx) <br/> |[OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) <br/> [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) , [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) <br/> |Возвращает ссылку на базовый XML-документ формы, состояние возврата и другие свойства, содержащие сведения о XML-узле во время изменения объектной модели XML-документа. Также включает метод выявления ошибок.  <br/> |
|[DocActionEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocActionEvent.aspx) <br/> |[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) <br/> |Возвращает ссылку на базовый XML-документ формы, статус возврата, а также исходный XML-узел во время нажатия кнопки в области формы.  <br/> |
|[DocContextChangeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocContextChangeEvent.aspx) <br/> |[OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx) <br/> |Возвращает информацию об XML-узле модели Document Object Model (DOM), который является текущим контекстом базового XML-документа формы.  <br/> |
|[DocEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocEvent.aspx) <br/> |[OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx) , [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) <br/> |Возвращает ссылку на базовый XML-документ формы во время переключения режимов или во время операции объединения форм.  <br/> |
|[DocReturnEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DocReturnEvent.aspx) <br/> |[OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) <br/> |Возвращает ссылку на базовый XML-документ формы, а также статус возврата в течение загрузки или отправки формы.  <br/> |
|[MergeEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MergeEvent.aspx) <br/> |[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) <br/> |Возвращает свойства и методы, которые можно использовать при выполнении события  **OnMergeRequest** для программного взаимодействия с базовым XML-документом формы, а также для определения свойств объединения, таких как число объединяемых файлов.  <br/> |
|[Савивент](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SaveEvent.aspx) <br/> |[OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) <br/> |Возвращает число свойств и методов, которые можно использовать во время сохранения из обработчика событий **OnSaveRequest** для программного взаимодействия с базовым XML-документом формы, определения свойств сохранения и выполнения сохранения.  <br/> |
|[Сигневент](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) <br/> |[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Используется для ввода дополнительных данных в цифровую подпись.  <br/> |
|[Версионупградивент](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.VersionUpgradeEvent.aspx) <br/> |[OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) <br/> |Возвращает ссылку на базовый XML-документ формы, статус возврата, а также номера версий документа и приложения во время обновления версии.  <br/> |
   
## <a name="using-the-event-objects"></a>Использование объектов событий

При создании обработчика событий приложение InfoPath создает объявление обработчика событий в файле кода формы проекта (FormCode.cs или FormCode.vb). В этом описании приложение InfoPath использует **e** в качестве имени параметра, передаваемого обработчику событий. Этот параметр содержит объект событий, который связан с обработчиком событий. 
  
Например, при создании обработчика событий **OnLoad** в режиме конструктора (выбрав **Событие OnLoad** на вкладке **Разработчик**) приложение InfoPath добавляет объявление обработчика событий, получающего объект **DocReturnEvent**, в файл кода формы, а затем открывает редактор кода, чтобы можно было добавить код в следующее объявление обработчика событий. 
  
```cs
// The following function handler is created by Microsoft Office 
// InfoPath. Do not modify the type or number of arguments.
[InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
public void FormEvents_OnLoad(DocReturnEvent e)
{
   // Write your code here.
}
```

```vb
' The following function handler is created by Microsoft Office 
' InfoPath. Do not modify the type or number of arguments.
<InfoPathEventHandler(EventType:=InfoPathEventType.OnLoad)> _
Public Sub FormEvents_OnLoad(ByVal e As DocReturnEvent)
   ' Write your code here.
End Sub
```

При написании кода для обработчика событий можно воспользоваться свойствами и методами, внедренными объектом события, переданным через параметр **e**. Например, в следующем обработчике события **OnBeforeChange** свойство [newValue](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.NewValue.aspx) объекта события **DataDOMEvent** используется для проверки значения поля, которое было только что изменено. Если он пуст, свойство [ReturnMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnMessage.aspx) объекта события **DataDOMEvent** используется для отображения ошибки для пользователя в диалоговом окне, а свойство [ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReturnStatus.aspx) имеет значение **false**, указывая, что изменения, внесенные пользователем, должны не принимается.
  
```cs
[InfoPathEventHandler(MatchPath="/my:myFields/my:field1", 
    EventType=InfoPathEventType.OnBeforeChange)]
public void field1_OnBeforeChange(DataDOMEvent e)
{
   // Determine whether there is a new value.
   if ((string)e.NewValue == "")
   {
      // The value is blank, so display an error message and roll
      // back the changes.
      e.ReturnMessage = "You must supply a value for this field.";
      e.ReturnStatus = false;
      return;
   }
}
```

```vb
<InfoPathEventHandler(MatchPath:="/my:myFields/my:field1", _ EventType:=InfoPathEventType.OnBeforeChange)> _
Public Sub field1_OnBeforeChange(ByVal e As DataDOMEvent)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message and roll back
      ' the changes.
      e.ReturnMessage = "You must supply a value for this field."
      e.ReturnStatus = False
      Return
   End If
End Sub
```

> [!NOTE]
> Каждый из объектов событий InfoPath в объектной модели, совместимой с InfoPath 2003, реализует различные свойства и методы. Для получения подробных сведений о конкретных объектах событий щелкните соответствующий объект в в приведенной ранее таблице объектов событий. 
  

