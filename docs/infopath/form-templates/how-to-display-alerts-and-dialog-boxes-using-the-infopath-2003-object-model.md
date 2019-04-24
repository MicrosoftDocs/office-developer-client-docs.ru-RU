---
title: Отображение оповещений и диалоговых окон с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны форм, совместимые с InfoPath 2003, отображение диалоговых окон, шаблонов форм [InfoPath 2007], отображение диалоговых окон, оповещений, отображение в шаблонах форм, совместимых с InfoPath 2003, диалоговые окна, отображение в шаблонах форм InfoPath, совместимых с 2003 , Шаблоны форм, совместимые с InfoPath 2003, отображение оповещений
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: При написании кода для расширения возможностей шаблона формы, использующего объектную модель InfoPath 2003, зачастую полезно предоставлять пользователю сведения в диалоговом окне.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303614"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Отображение оповещений и диалоговых окон с помощью объектной модели InfoPath 2003

При написании кода для расширения возможностей шаблона формы, использующего объектную модель InfoPath 2003, зачастую полезно предоставлять пользователю сведения в диалоговом окне. Программное отображение диалогового окна и связанных элементов пользовательского интерфейса выполняется в InfoPath с помощью методов интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
## <a name="overview-of-the-uiobject-interface"></a>Обзор интерфейса UIObject

Интерфейс [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) предоставляет следующие методы, которые разработчики форм могут использовать для отображения различных типов диалоговых окон для пользователей InfoPath при заполнении формы. 
  
|Имя|Описание|
|:-----|:-----|
|[Акций](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Отображает простое окно сообщения, содержащее указанную строку сообщения. Этот метод следует использовать в том случае, если от пользователя не требуется ввода данных, а нужно только отобразить сообщение. Отображенное диалоговое окно закрывается путем нажатия кнопки **ОК**.<br/> |
|[Confirm](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Отображает окно сообщения с кнопками для ввода данных. Возвращаемое значение является одной из перечислимых констант [ксдконфирмчоице](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Задает имя по умолчанию для формы в диалоговом окне **Сохранить как**.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Задает исходное расположение обзора при открытии диалогового окна **Сохранить как**.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Создает новое сообщение электронной почты в почтовом приложении по умолчанию с открытой в данный момент формой, вложенной в сообщение.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Отображает модальное диалоговое окно, основываясь на указанном HTML-файле и позиционных аргументах. Этот метод следует использовать, если вы хотите, чтобы пользователь отображал больше простого сообщения, и вам нужно получить данные от пользователя (помимо простого подтверждения, предоставленного при нажатии **кнопки Да** ). | **Нет** | **Отмена** кнопок, отображаемых методом **Confirm** .  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Отображает встроенное диалоговое окно **Цифровые подписи**.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Использование интерфейса UIObject

Доступ к интерфейсу [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) осуществляется через свойство [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , доступ к которому осуществляется с помощью `thisXDocument` переменной, инициализированной в `_Startup` методе класса кода формы. В следующем примере показано использование методов [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) и [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
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

В этом примере показано, как использовать метод [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) для отображения настраиваемого диалогового окна, определенного в HTML-файле Show. HTML. 
  
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

Примеры Visual C# и Visual Basic зависят от HTML-файла с именем "Show. HTML", определяющего диалоговое окно, которое вызывается методом [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) . В этом HTML-файле отображаются некоторые данные из формы и выводится текстовое поле для заполнения пользователем. Значение текстового поля возвращается в форму при закрытии диалогового окна. 
  
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
> Метод [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) требует полного доверия для запуска или предварительной версии. Дополнительные сведения можно найти в статье [Просмотр и отладка шаблонов форм, требующИх полного доверия](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

