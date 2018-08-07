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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="4b299-104">Отображение оповещений и диалоговых окон с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="4b299-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="4b299-105">При создании кода для расширения функциональности шаблона формы, который использует объектную модель InfoPath 2003, часто бывает полезно предоставить пользователю сведения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4b299-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="4b299-106">Программная отображение диалоговое окно и связанные элементы интерфейса выполняется в InfoPath с помощью методов интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b299-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="4b299-107">Обзор интерфейса UIObject</span><span class="sxs-lookup"><span data-stu-id="4b299-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="4b299-108">Интерфейс [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) предоставляет следующие методы, которые могут использоваться разработчиками форм для отображения различных типов диалоговых окон, отображаемых для пользователей InfoPath при заполнении формы.</span><span class="sxs-lookup"><span data-stu-id="4b299-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="4b299-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4b299-109">Name</span></span>|<span data-ttu-id="4b299-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4b299-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b299-111">Alert</span><span class="sxs-lookup"><span data-stu-id="4b299-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="4b299-p102">Отображает простое окно сообщения, содержащее указанную строку сообщения. Этот метод следует использовать в том случае, если от пользователя не требуется ввода данных, а нужно только отобразить сообщение. Отображенное диалоговое окно закрывается путем нажатия кнопки **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b299-p102">Displays a simple message box that contains a specified message string. This method should be used when no input is required from the user and only a message needs to be displayed. The dialog box displayed is closed by clicking the **OK** button.  </span></span><br/> |
|[<span data-ttu-id="4b299-115">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="4b299-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="4b299-116">Отображает окно сообщения с кнопками для ввода данных.</span><span class="sxs-lookup"><span data-stu-id="4b299-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="4b299-117">Значение, возвращаемое является одной из констант перечисления [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b299-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="4b299-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="4b299-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="4b299-119">Задает имя файла по умолчанию для формы в диалоговом окне **Сохранить как**. </span><span class="sxs-lookup"><span data-stu-id="4b299-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="4b299-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="4b299-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="4b299-121">Задает исходное расположение обзора при открытии диалогового окна **Сохранить как**. </span><span class="sxs-lookup"><span data-stu-id="4b299-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="4b299-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="4b299-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="4b299-123">Создает новое сообщение электронной почты в приложении электронной почты по умолчанию, с текущей открытой формы вложения в сообщение.</span><span class="sxs-lookup"><span data-stu-id="4b299-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="4b299-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="4b299-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="4b299-125">Отображает модальное диалоговое окно, на основе указанного HTML-файла и аргументы.</span><span class="sxs-lookup"><span data-stu-id="4b299-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="4b299-126">Этот метод следует использовать, если необходимо отобразить более простое сообщение пользователю, и требуется получить некоторые данные от пользователя (за пределы простого подтверждения, предоставленные **Да**</span><span class="sxs-lookup"><span data-stu-id="4b299-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="4b299-127">**Нет**</span><span class="sxs-lookup"><span data-stu-id="4b299-127">**No**</span></span> | <span data-ttu-id="4b299-128">**Отменить** кнопок, отображаемых с помощью метода **Confirm** ).</span><span class="sxs-lookup"><span data-stu-id="4b299-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="4b299-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="4b299-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="4b299-130">Отображает встроенное диалоговое окно **Цифровые подписи**.</span><span class="sxs-lookup"><span data-stu-id="4b299-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="4b299-131">Использование интерфейса UIObject</span><span class="sxs-lookup"><span data-stu-id="4b299-131">Using the UIObject Interface</span></span>

<span data-ttu-id="4b299-132">Интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) доступен через свойство [пользовательский Интерфейс](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) интерфейс [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , который доступен через `thisXDocument` переменную, которая инициализируется в `_Startup` метод класса кода формы.</span><span class="sxs-lookup"><span data-stu-id="4b299-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="4b299-133">В следующем примере с помощью методов интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) и [оповещения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b299-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="4b299-134">Использование интерфейса ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="4b299-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="4b299-135">В этом примере показано, как использовать метод [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) интерфейса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) для отображения настраиваемого диалогового окна определенного в HTML-файле show.html.</span><span class="sxs-lookup"><span data-stu-id="4b299-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="4b299-136">Примеры Visual C# и Visual Basic зависят от HTML-файл с именем «show.html», который определяет поле, которая вызывается с помощью метода [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b299-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="4b299-137">В этом HTML-файл отображаются некоторые данные из формы и отображает текстовое поле, пользователь может ввести значение.</span><span class="sxs-lookup"><span data-stu-id="4b299-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="4b299-138">При закрытии диалоговое окно, в форму возвращается значение в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="4b299-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="4b299-139">Метод [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) требуется полное доверие для запуска или предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="4b299-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="4b299-140">Для получения дополнительных сведений см. [Просмотр и отладка шаблонов форм, требуется полное доверие](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="4b299-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

