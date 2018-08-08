---
title: Устранение неполадок шаблонов форм, использующих объектную модель InfoPath во время разработки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, troubleshooting at design time,troubleshooting form templates [InfoPath 2007], design time
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: В следующих разделах описываются распространенные сценарии устранения неполадок, которые могут встретиться при разработке и отладке шаблонов форм с управляемым кодом, использующих объектную модель, совместимую с InfoPath 2003, которая предоставляется пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust.
ms.openlocfilehash: af71c8058744561a4c8ee0870fb37054e9979751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807593"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Устранение неполадок шаблонов форм, использующих объектную модель InfoPath во время разработки

В следующих разделах описываются распространенные сценарии устранения неполадок, которые могут встретиться при разработке и отладке шаблонов форм с управляемым кодом, использующих объектную модель, совместимую с InfoPath 2003, которая предоставляется пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust**. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Не удается просмотреть или отладить шаблоны форм, использующие вызовы методов и свойств объектной модели с уровнем безопасности 3

При попытке отладки или предварительного просмотра проекта управляемого кода, который содержит код, который вызывает элементы объектной модели, требующих полного доверия, InfoPath будет отображаться сообщение об ошибке «в коде формы произошло исключение необработанное безопасности» и форма не будет открываться . Чтобы разрешить бизнес-логика в шаблоне формы для отладки или предварительного просмотра, необходимо установить уровень безопасности **Полное доверие** и использовать цифровую подпись шаблона формы. Для получения дополнительных сведений о том, как это сделать см [Просмотр и отладка шаблонов форм, требуется полное доверие](how-to-preview-and-debug-form-templates-that-require-full-trust.md).
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>Не удается обновить выражения XPath в обработчиках событий, если значение параметра "MatchPath" было удалено вручную

Если добавить обработчик событий для поля или группы и впоследствии изменить схемы источника данных в области задач InfoPath **полей** , чтобы влияет на этого поля или группы (например, по переименованию или перемещению его), сообщение будет отображаться вопросом, следует ли обновлено e XPath выражений в коде формы. Выражения XPath, приведенные в этом сообщении являются значения, заданные с помощью параметра ["matchpath"](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) атрибута [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) , используемые для связи обработчика событий с помощью поля или группы в источник данных для формы . Другие выражения XPath в коде не будут обновлены. Алгоритм для обновления выражения XPath зависит от значения, этот параметр указан с помощью параметра **"matchpath"** **InfoPathEventHandler** атрибутов, которые применяются в коде формы. Если эти значения удалены вручную перед ответом на запрос на обновление выражения XPath, InfoPath не сможет автоматически обновить выражения XPath. Дополнительные сведения можно [Добавить события обработчик с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Не удается вызвать элементы объектной модели, совместимой с InfoPath 2003, в отдельном потоке

Объектная модель, совместимая с InfoPath 2003, не поддерживает вызовы в отдельном потоке. Например, следующий код, вызывающий функцию LaunchOMFunction, которая вызывает элементы объектной модели InfoPath, не запустится. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

При необходимости существует возможность обойти это ограничение. Дополнительные сведения см. в статье [Поддержка потоков в проектах InfoPath, использующих объектную модель InfoPath 2003](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>Пропуск необязательных параметров приводит к ошибке построения в Visual Basic и Visual C#

Если элемент объектной модели InfoPath содержит необязательный параметр и значение этого параметра не указано, то необходимо передать для этого параметра поле **Type.Missing**. Если не передать поле **Type.Missing** при пропуске фактического значения, произойдет ошибка построения. Это применимо к коду, написанному как на Visual Basic, так и на Visual C#. Дополнительные сведения и примеры см. в подразделе "Передача необязательных параметров для элементов объектной модели InfoPath" раздела [Объектные модели, совместимые с InfoPath 2003](infopath-2003-compatible-object-models.md). 
  
## <a name="see-also"></a>См. также

- [Сведения о модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md)
- [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md)
- [Обработка ошибок с помощью объектной модели InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Просмотр и отладка шаблонов форм, требующих полного доверия](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Отладка проектов InfoPath, использующих объектную модель InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

