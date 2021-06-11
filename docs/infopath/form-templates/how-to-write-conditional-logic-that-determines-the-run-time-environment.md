---
title: Записывая условная логика, определяемая средой запуска
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- запущенная в infopath [infopath 2007], временная среда [InfoPath 2007], запущенная в браузере [InfoPath 2007],InfoPath 2007, определяя временную среду
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Свойство Environment класса Application получает ссылку на объект Environment, который можно использовать для определения среды запуска (InfoPath, веб-браузер или мобильный браузер) для открытия формы.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408602"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Записывая условная логика, определяемая средой запуска

Свойство [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) получает ссылку на объект [Environment,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) который можно использовать для определения среды запуска (InfoPath, веб-браузер или мобильный браузер) для открытия формы. 
  
## <a name="example"></a>Пример

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Определение среды выполнения, в которой запускается форма

Класс [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) предоставляет свойства [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) и [IsMobile,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) которые позволяют определить, какая среда редактирования использовалась для открытия шаблона формы. Если оба свойства возвращаются **ложными,** шаблон формы был открыт в редакторе Microsoft InfoPath. Если Microsoft SharePoint Server 2010 InfoPath Forms Services года в программе соответствующего свойства: веб-браузер[(свойство IsBrowser)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) или мобильный браузер [(свойство IsMobile).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx)  
  
Если в следующем примере форма открывается в веб-браузере или в браузере мобильного устройства, то для значения field1 (связанное с элементом управления **Текстовое поле**) устанавливается строка, указывающая среду выполнения, в которой выполнялось открытие формы. Если форма открывается в InfoPath, то для отображения окна сообщения используется метод **System.Windows.Forms.MessageBox.Show** (который недоступен при запуске формы в веб-браузере). 
  
> [!IMPORTANT]
> При создании шаблона формы для следующего примера  кода выберите пустой шаблон на вкладке **New** of the Backstage view. (Кроме того, вы  можете выбрать  форму веб-браузера из  выпадаемого списка типа формы в категории Совместимость диалоговой окне **Параметры** формы.) Чтобы поддерживать **класс MessageBox,** добавьте ссылку на **System.Windows. Формы** на . **Вкладка NET** в диалоговом окне Add **Reference** в Visual Studio 2012 г., а затем добавьте директиву об использовании или импорте для   **System.Windows. Формы** в разделе объявления модуля кода формы. 
  
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


