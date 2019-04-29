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
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="44194-104">Написание условной логики, определяющей среду выполнения</span><span class="sxs-lookup"><span data-stu-id="44194-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="44194-105">Свойство [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) получает ссылку на объект [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , который можно использовать для определения того, какая среда выполнения (InfoPath, веб-браузер или браузер мобильного устройства) использовалась для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="44194-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="44194-106">Пример</span><span class="sxs-lookup"><span data-stu-id="44194-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="44194-107">Определение среды выполнения, в которой запускается форма</span><span class="sxs-lookup"><span data-stu-id="44194-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="44194-108">Класс [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) предоставляет свойства [Browser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) и для [мобильных устройств](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , которые позволяют определить, какая среда редактирования использовалась для открытия шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="44194-108">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template.</span></span> <span data-ttu-id="44194-109">Если оба свойства возвращают **значение false**, шаблон формы был открыт в редакторе Microsoft InfoPath.</span><span class="sxs-lookup"><span data-stu-id="44194-109">If both properties return **false**, the form template was opened in the Microsoft InfoPath editor.</span></span> <span data-ttu-id="44194-110">Если любое свойство возвращает **значение true**, шаблон формы был открыт из соответствующей настроенной библиотеки документов в Microsoft SharePoint Server 2010, на котором запущены службы InfoPath Forms Services в программе для соответствующего свойства: веб-браузер ([ Свойство Browser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ) или веб-браузер для мобильных [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) устройств (свойство для мобильных устройств).</span><span class="sxs-lookup"><span data-stu-id="44194-110">If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="44194-111">Если в следующем примере форма открывается в веб-браузере или в браузере мобильного устройства, то для значения field1 (связанное с элементом управления **Текстовое поле**) устанавливается строка, указывающая среду выполнения, в которой выполнялось открытие формы.</span><span class="sxs-lookup"><span data-stu-id="44194-111">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in.</span></span> <span data-ttu-id="44194-112">Если форма открывается в InfoPath, то для отображения окна сообщения используется метод **System.Windows.Forms.MessageBox.Show** (который недоступен при запуске формы в веб-браузере).</span><span class="sxs-lookup"><span data-stu-id="44194-112">If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="44194-113">При создании шаблона формы для следующего образца кода выберите **пустой** шаблон на вкладке **создать** представления Backstage.</span><span class="sxs-lookup"><span data-stu-id="44194-113">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view.</span></span> <span data-ttu-id="44194-114">(Кроме того, вы можете выбрать **форму веб-браузера** в раскрывающемся списке **тип формы** под категорией **Совместимость** в диалоговом окне **Параметры формы** .) Чтобы обеспечить поддержку класса **MessageBox** , добавьте ссылку на **System. Windows. Forms** на странице.</span><span class="sxs-lookup"><span data-stu-id="44194-114">(Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the .</span></span> <span data-ttu-id="44194-115">Вкладка " **сеть** " диалогового окна " **Добавление ссылки** " в Visual Studio 2012, а затем добавьте директиву **using** или **Imports** для **System. Windows. Forms** в разделе объявления модуля кода формы.</span><span class="sxs-lookup"><span data-stu-id="44194-115">**NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
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


