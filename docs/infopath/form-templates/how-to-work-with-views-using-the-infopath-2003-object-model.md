---
title: Работа с представлениями с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, views,views [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель, совместимая с InfoPath 2003, поддерживает доступ к представлениям формы с помощью членов интерфейса ViewObject.
ms.openlocfilehash: 6a2dd408ba51e5c8394120944e0c28897e768738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411885"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Работа с представлениями с помощью объектной модели InfoPath 2003

При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель, совместимая с InfoPath 2003, поддерживает доступ к представлениям формы с помощью членов [интерфейса ViewObject.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) 
  
## <a name="overview-of-the-viewobject-interface"></a>Обзор интерфейса ViewObject

Интерфейс [ViewObject предоставляет](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) следующие методы и свойства, которые разработчики форм могут использовать для взаимодействия с представлением InfoPath. 
  
> [!NOTE]
> Методы и свойства интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) недоступны во время события [OnLoad.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) 
  
|**Название**|**Описание**|
|:-----|:-----|
|[Метод DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Отключает синхронизацию модели XML DOM и представления.  <br/> |
|[Метод EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Включает синхронизацию модели XML DOM и представления.  <br/> |
|[Метод ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx)  <br/> |Выполняет действие редактирования InfoPath.  <br/> |
|[Метод Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)  <br/> |Экспортирует представление в файл указанного формата.  <br/> |
|[Метод ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Синхронизирует модель XML DOM и представление.  <br/> |
|[Метод GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на интерфейс [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) на основе указанного узла XML и контекста представления или текущего выделения в представлении.  <br/> |
|[Метод GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Возвращает ссылку на интерфейс **XMLNodesCollection**, основываясь на текущем выделении в представлении.  <br/> |
|[Метод SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx)  <br/> |Выбирает диапазон XML-узлов в представлении.  <br/> |
|[Метод SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)  <br/> |Выбирает текст, содержащийся в указанном XML-узле в представлении.  <br/> |
|[Метод SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)  <br/> |Переключает форму InfoPath в указанное представление.  <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)  <br/> |Возвращает строковое значение, указывающее имя текущего представления.  <br/> |
|[Свойство Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx)  <br/> |Возвращает ссылку на интерфейс [WindowObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) который имеет доступ к **окну,** связанному с представлением.  <br/> |
   
> [!NOTE]
> Объектная модель, совместимая с InfoPath 2003, также предоставляет интерфейс [ViewInfosCollection,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) который можно использовать для получения сведений обо всех представлениях, реализованных в форме. 
  
## <a name="using-the-viewobject-interface"></a>Использование интерфейса ViewObject

Доступ к интерфейсу [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) можно получить с помощью свойства [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (доступ к которому можно получить с помощью переменной, инициализированной в методе класса  `thisXDocument` кода  `_Startup` формы). Например, в следующем примере кода показано, как использовать метод [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) для отображения окна сообщения с именем текущего представления, связанного с XML-документом формы. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Все формы InfoPath содержат по крайней мере одно представление по умолчанию; Однако InfoPath также поддерживает создание нескольких представлений XML-документа формы. Если в форме несколько представлений, объект **View** можно использовать для работы с текущим активным представлением. Вы можете программным способом изменить активное представление с помощью метода **SwitchView** объекта **View,** как показано в следующем примере кода. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

Предыдущий пример по переключению представления будет работать только после открытия формы. Чтобы установить представление по умолчанию во время события **OnLoad,** используйте свойство [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) интерфейса [ViewInfoObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) как показано в следующем примере. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


