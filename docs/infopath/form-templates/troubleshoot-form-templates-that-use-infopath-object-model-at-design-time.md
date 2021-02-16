---
title: Устранение неполадок шаблонов форм, которые используют объектную модель InfoPath во время разработки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, troubleshooting at design time,troubleshooting form templates [InfoPath 2007], design time
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: В следующих разделах описываются распространенные сценарии устранения неполадок, которые могут встретиться при разработке и отладке шаблонов форм с управляемым кодом, использующих объектную модель, совместимую с InfoPath 2003, которая предоставляется пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: 106f12602bae86d85c2a7d2f920f59d50326c908
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436526"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Устранение неполадок шаблонов форм, которые используют объектную модель InfoPath во время разработки

В следующих разделах описываются распространенные сценарии устранения неполадок, которые могут встретиться при разработке и отладке шаблонов форм с управляемым кодом, использующих объектную модель, совместимую с InfoPath 2003, которая предоставляется пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust**. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Не удается просмотреть или отладить шаблоны форм, использующие вызовы методов и свойств объектной модели с уровнем безопасности 3

При попытке отладить или просмотреть проект с управляемым кодом, вызывающим элементы объектной модели, для которых требуется полное доверие, приложение InfoPath отобразит сообщение об ошибке "В форме кода произошло необработанное исключение безопасности" и форма не откроется. Чтобы разрешить отладку и просмотр бизнес-логики шаблона формы, необходимо установить уровень безопасности **Полное доверите** и указать для шаблона формы цифровую подпись. Дополнительные сведения о том, как это сделать, см. в предварительных и отлачивых шаблонах форм, для работы с которые [требуется полное доверие.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Не удается обновить выражения XPath в обработчиках событий, если значение параметра "MatchPath" было удалено вручную

Если вы добавляете обработок событий в поле или группу, а затем измените схему источника данных в области задач "Поля **InfoPath"** таким образом, чтобы он влиял на это поле или группу (например, путем переименования или перемещения), отобразилось сообщение с запросом на обновление выражений XPath в коде формы. Выражения XPath, указанные в этом сообщении, являются значениями, указанными в параметре [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) атрибута [InfoPathEventHandlerAttribute,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) которые используются для связи обработца событий с полем или группой в источнике данных формы. Другие выражения XPath в коде не будут обновляться. Алгоритм обновления выражений XPath зависит от значения, которое присутствует в параметре **MatchPath** атрибутов **InfoPathEventHandler,** применяемых в коде формы. Если вы удалили эти значения вручную перед ответом на запрос на обновление выражений XPath, InfoPath не сможет автоматически обновлять выражения XPath. Дополнительные сведения см. в подразделе [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Не удается вызвать элементы объектной модели, совместимой с InfoPath 2003, в отдельном потоке

Объектная модель, совместимая с InfoPath 2003, не поддерживает вызовы в отдельном потоке. Например, следующий код, вызывающий функцию LaunchOMFunction, которая вызывает элементы объектной модели InfoPath, не запустится. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

При необходимости существует возможность обойти это ограничение. Сведения см. в [подразделе "Поддержка потоков в проектах InfoPath с использованием объектной модели InfoPath 2003".](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>Пропуск необязательных параметров приводит к ошибке построения в Visual Basic и Visual C#

Если элемент объектной модели InfoPath содержит необязательный параметр и значение этого параметра не указано, то необходимо передать для этого параметра поле **Type.Missing**. Если не произвести передачу поля **Type.Missing**, когда его фактическое значение опущено, это может привести к ошибке построения. Это применимо к коду, написанному как на Visual Basic, так и на Visual C#. Дополнительные сведения и примеры см. в разделе "Передача необязательных параметров членам объектной модели InfoPath" в разделе "Объектные модели, совместимые [с InfoPath 2003".](infopath-2003-compatible-object-models.md) 
  
## <a name="see-also"></a>См. также

- [О модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md)
- [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md)
- [Обработка ошибок с помощью объектной модели InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Предварительный просмотр и отлагивание шаблонов форм, которые требуют полного доверия](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Отлаживать проекты InfoPath с помощью объектной модели InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

