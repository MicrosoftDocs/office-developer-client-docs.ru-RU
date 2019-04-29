---
title: Написание условной логики, определяющей среду выполнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- работа в InfoPath [InfoPath 2007], среда выполнения [InfoPath 2007], работа в браузере [InfoPath 2007], InfoPath 2007, определение среды выполнения
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Свойство Environment класса Application получает ссылку на объект Environment, который можно использовать для определения того, какая среда выполнения (InfoPath, веб-браузер или браузер мобильного устройства) использовалась для открытия формы.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408602"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Написание условной логики, определяющей среду выполнения

Свойство [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) получает ссылку на объект [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , который можно использовать для определения того, какая среда выполнения (InfoPath, веб-браузер или браузер мобильного устройства) использовалась для открытия формы. 
  
## <a name="example"></a>Пример

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Определение среды выполнения, в которой запускается форма

Класс [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) предоставляет свойства [Browser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) и для [мобильных устройств](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , которые позволяют определить, какая среда редактирования использовалась для открытия шаблона формы. Если оба свойства возвращают **значение false**, шаблон формы был открыт в редакторе Microsoft InfoPath. Если любое свойство возвращает **значение true**, шаблон формы был открыт из соответствующей настроенной библиотеки документов в Microsoft SharePoint Server 2010, на котором запущены службы InfoPath Forms Services в программе для соответствующего свойства: веб-браузер ([ Свойство Browser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ) или веб-браузер для мобильных [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) устройств (свойство для мобильных устройств). 
  
Если в следующем примере форма открывается в веб-браузере или в браузере мобильного устройства, то для значения field1 (связанное с элементом управления **Текстовое поле**) устанавливается строка, указывающая среду выполнения, в которой выполнялось открытие формы. Если форма открывается в InfoPath, то для отображения окна сообщения используется метод **System.Windows.Forms.MessageBox.Show** (который недоступен при запуске формы в веб-браузере). 
  
> [!IMPORTANT]
> При создании шаблона формы для следующего образца кода выберите **пустой** шаблон на вкладке **создать** представления Backstage. (Кроме того, вы можете выбрать **форму веб-браузера** в раскрывающемся списке **тип формы** под категорией **Совместимость** в диалоговом окне **Параметры формы** .) Чтобы обеспечить поддержку класса **MessageBox** , добавьте ссылку на **System. Windows. Forms** на странице. Вкладка " **сеть** " диалогового окна " **Добавление ссылки** " в Visual Studio 2012, а затем добавьте директиву **using** или **Imports** для **System. Windows. Forms** в разделе объявления модуля кода формы. 
  
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


