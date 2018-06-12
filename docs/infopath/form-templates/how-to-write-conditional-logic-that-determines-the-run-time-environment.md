---
title: Запись условную логику, определяющую среды выполнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- выполнение в infopath [infopath 2007], среда выполнения [InfoPath 2007], работающей в браузере [InfoPath 2007], InfoPath 2007, определение среды выполнения
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Свойство среды класса приложение получает ссылку на объект среды, который можно использовать, чтобы определить, какой среде выполнения (InfoPath, веб-браузер или браузер мобильного телефона) использовалась при открытии формы.
ms.openlocfilehash: b854d6a3b65fcc37375480bef9f1909d84407b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807496"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Запись условную логику, определяющую среды выполнения

Свойство [среды](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) класса [приложение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) получает ссылку на объект [среды](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , который можно использовать, чтобы определить, какой среде выполнения (InfoPath, веб-браузер или браузер мобильного телефона) использовалась при открытии формы. 
  
## <a name="example"></a>Пример

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Определение среды выполнения, в которой запускается форма

Класс [среды](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) предоставляет свойства [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) и [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , которые позволяют определить, какая среда редактирования использовалось для открытия шаблона формы. Если оба свойства возвращают **значение false**, шаблон формы был открыт в редакторе Microsoft InfoPath. Если одно из свойств возвращает **значение true**, шаблон формы был открыт из соответственно настроенной библиотеки документов на сервере Microsoft SharePoint Server 2010 под управлением службы InfoPath Forms Services в программе для соответствующего свойства: веб-браузера ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) свойство) или браузер мобильного телефона (свойство [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ). 
  
В следующем примере Если форма открыта в браузере или браузеров мобильных устройств field1 (который привязан к элемент управления **Текстовое поле** ) — это значение к типу string указывает, какой среде выполнения, форма была открыта в. Если форма открыта в InfoPath, метод **System.Windows.Forms.MessageBox.Show** (который недоступен, когда форма открыта в браузере) используется для отображения окна сообщения. 
  
> [!IMPORTANT]
> При создании шаблона формы для в следующем образце кода выберите **пустой** шаблон на вкладке **Создать** в представлении Backstage. (Кроме того, можно выбрать **Форма веб-браузера** в раскрывающемся списке **тип формы** в разделе категория **Совместимость** диалогового окна **Параметры формы** .) Чтобы обеспечить поддержку класс **MessageBox** , добавьте ссылку на **System.Windows.Forms** на. Вкладка **NET** диалогового окна **Добавить ссылку на** поле в Visual Studio 2012, а затем добавьте директива **using** или **Imports** для **System.Windows.Forms** в разделе объявлений модуля кода формы. 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


