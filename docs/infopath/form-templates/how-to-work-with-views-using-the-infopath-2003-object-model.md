---
title: Работа с представлениями, использующих объектную модель InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны форм с поддержкой 2003 InfoPath, представлений, представлений [InfoPath 2007], совместимых с InfoPath 2003 шаблонов форм
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: При работе с шаблона формы InfoPath можно написать код для доступа к представлениям формы и выполните ряд действий на данные, которые содержат представления. Объектная модель совместимых с InfoPath 2003 поддерживает доступ к представлений формы посредством использования члены интерфейса ViewObject.
ms.openlocfilehash: 1cbc472993ff18b26f31e3bc28b12a75e559644a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807507"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Работа с представлениями, использующих объектную модель InfoPath 2003

При работе с шаблона формы InfoPath можно написать код для доступа к представлениям формы и выполните ряд действий на данные, которые содержат представления. Объектная модель совместимых с InfoPath 2003 поддерживает доступ к представлений формы посредством использования члены интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) . 
  
## <a name="overview-of-the-viewobject-interface"></a>Обзор интерфейса ViewObject

Интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с представлением InfoPath. 
  
> [!NOTE]
> Методы и свойства интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) недоступны во время события [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) . 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Отключает синхронизацию модели XML DOM и представления.  <br/> |
|Метод [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Включает синхронизацию модели XML DOM и представления.  <br/> |
|Метод [ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx)  <br/> |Выполняет действие редактирования InfoPath.  <br/> |
|Метод [Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)  <br/> |Экспортирует представление в файл указанного формата.  <br/> |
|Метод [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Синхронизирует модель XML DOM и представление.  <br/> |
|Метод [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на интерфейс [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) , основываясь на указанном XML узле и контексте представления или текущем выделении в представлении.  <br/> |
|Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Возвращает ссылку на интерфейс **XMLNodesCollection** , основываясь на текущем выделении в представлении.  <br/> |
|Метод [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx)  <br/> |Выбирает диапазон XML-узлов в представлении.  <br/> |
|Метод [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)  <br/> |Выбирает текст, содержащийся в указанном XML-узле в представлении.  <br/> |
|Метод [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)  <br/> |Переключает форму InfoPath в указанное представление.   <br/> |
|Свойство [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)  <br/> |Возвращает строковое значение, указывающее имя текущего представления.  <br/> |
|Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx)  <br/> |Возвращает ссылку на интерфейс [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) , который осуществляет доступ к **окно** , связанное с представлением.  <br/> |
   
> [!NOTE]
> Объектная модель совместимых с InfoPath 2003 также предоставляет интерфейс [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) , который можно использовать для получения сведений обо всех представлениях, реализованных в форме. 
  
## <a name="using-the-viewobject-interface"></a>Использование интерфейса ViewObject

Интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) доступен через свойство [представления](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) (которого осуществляется с помощью `thisXDocument` переменную, которая инициализируется в `_Startup` метод класса кода формы). Например в следующем примере кода показано, как [оповещения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) метод интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) используется для отображения окна сообщения с именем текущего представления, связанного с XML-документом формы. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Все формы InfoPath содержат по крайней мере один представление по умолчанию; Тем не менее InfoPath поддерживает создание нескольких представлений формы XML-документом. При наличии нескольких представлений в форме объект **представления** можно использовать для работы с представлением активной. Программными средствами можно изменить представление, в настоящее время активной, используя метод **SwitchView** объекта **View** , как показано в следующем примере кода. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

Для предыдущего примера для переключения представления будут работать только после открыта форма. Чтобы задать представление по умолчанию во время события **OnLoad** , используйте свойство [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) интерфейс [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) , как показано в следующем примере. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


