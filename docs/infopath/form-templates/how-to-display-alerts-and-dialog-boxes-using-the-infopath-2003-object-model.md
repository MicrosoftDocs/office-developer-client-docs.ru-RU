---
title: Отображение оповещений и диалоговых окон с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны [InfoPath 2007], отображение диалоговых окон, оповещения, форм шаблонов форм с поддержкой веб-2003 InfoPath, отображение диалоговых окон, отображение в шаблонах форм совместимых с InfoPath 2003, шаблоны форм диалоговых окон, отображение в совместимых с InfoPath 2003 , Шаблоны форм, совместимые с InfoPath 2003, отображение оповещений
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: При создании кода для расширения функциональности шаблона формы, который использует объектную модель InfoPath 2003, часто бывает полезно предоставить пользователю сведения в диалоговом окне.
ms.openlocfilehash: 1cc0f4c7a6696eae2d3b7058898b4119cede79e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807498"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Отображение оповещений и диалоговых окон с помощью объектной модели InfoPath 2003

При создании кода для расширения функциональности шаблона формы, который использует объектную модель InfoPath 2003, часто бывает полезно предоставить пользователю сведения в диалоговом окне. Программная отображение диалоговое окно и связанные элементы интерфейса выполняется в InfoPath с помощью методов интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
## <a name="overview-of-the-uiobject-interface"></a>Обзор интерфейса UIObject

Интерфейс [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) предоставляет следующие методы, которые могут использоваться разработчиками форм для отображения различных типов диалоговых окон, отображаемых для пользователей InfoPath при заполнении формы. 
  
|Имя|Описание|
|:-----|:-----|
|[Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Отображает простое окно сообщения, содержащее указанную строку сообщения. Этот метод следует использовать в том случае, если от пользователя не требуется ввода данных, а нужно только отобразить сообщение. Отображенное диалоговое окно закрывается путем нажатия кнопки **ОК**.<br/> |
|[Подтверждение](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Отображает окно сообщения с кнопками для ввода данных. Значение, возвращаемое является одной из констант перечисления [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Задает имя файла по умолчанию для формы в диалоговом окне **Сохранить как**.   <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Задает исходное расположение обзора при открытии диалогового окна **Сохранить как**.   <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Создает новое сообщение электронной почты в приложении электронной почты по умолчанию, с текущей открытой формы вложения в сообщение.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Отображает модальное диалоговое окно, на основе указанного HTML-файла и аргументы. Этот метод следует использовать, если необходимо отобразить более простое сообщение пользователю, и требуется получить некоторые данные от пользователя (за пределы простого подтверждения, предоставленные **Да** | **Нет** | **Отменить** кнопок, отображаемых с помощью метода **Confirm** ).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Отображает встроенное диалоговое окно **Цифровые подписи**.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Использование интерфейса UIObject

Интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) доступен через свойство [пользовательский Интерфейс](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) интерфейс [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , который доступен через `thisXDocument` переменную, которая инициализируется в `_Startup` метод класса кода формы. В следующем примере с помощью методов интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) и [оповещения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) . 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a>Использование интерфейса ShowModalDialog

В этом примере показано, как использовать метод [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) для отображения настраиваемого диалогового окна определенного в HTML-файле show.html. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

Примеры Visual C# и Visual Basic зависят от HTML-файл с именем «show.html», который определяет поле, которая вызывается с помощью метода [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . В этом HTML-файл отображаются некоторые данные из формы и отображает текстовое поле, пользователь может ввести значение. При закрытии диалоговое окно, в форму возвращается значение в текстовом поле. 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> Метод [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) требуется полное доверие для запуска или предварительного просмотра. Для получения дополнительных сведений см. [Просмотр и отладка шаблонов форм, требуется полное доверие](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

