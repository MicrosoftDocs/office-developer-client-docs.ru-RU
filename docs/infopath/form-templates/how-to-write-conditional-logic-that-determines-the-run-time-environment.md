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
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="42dbf-104">Запись условную логику, определяющую среды выполнения</span><span class="sxs-lookup"><span data-stu-id="42dbf-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="42dbf-105">Свойство [среды](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) класса [приложение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) получает ссылку на объект [среды](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , который можно использовать, чтобы определить, какой среде выполнения (InfoPath, веб-браузер или браузер мобильного телефона) использовалась при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="42dbf-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="42dbf-106">Пример</span><span class="sxs-lookup"><span data-stu-id="42dbf-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="42dbf-107">Определение среды выполнения, в которой запускается форма</span><span class="sxs-lookup"><span data-stu-id="42dbf-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="42dbf-108">Класс [среды](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) предоставляет свойства [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) и [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , которые позволяют определить, какая среда редактирования использовалось для открытия шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="42dbf-108">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template.</span></span> <span data-ttu-id="42dbf-109">Если оба свойства возвращают **значение false**, шаблон формы был открыт в редакторе Microsoft InfoPath.</span><span class="sxs-lookup"><span data-stu-id="42dbf-109">If both properties return **false**, the form template was opened in the Microsoft InfoPath editor.</span></span> <span data-ttu-id="42dbf-110">Если одно из свойств возвращает **значение true**, шаблон формы был открыт из соответственно настроенной библиотеки документов на сервере Microsoft SharePoint Server 2010 под управлением службы InfoPath Forms Services в программе для соответствующего свойства: веб-браузера ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) свойство) или браузер мобильного телефона (свойство [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="42dbf-110">If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="42dbf-111">В следующем примере Если форма открыта в браузере или браузеров мобильных устройств field1 (который привязан к элемент управления **Текстовое поле** ) — это значение к типу string указывает, какой среде выполнения, форма была открыта в.</span><span class="sxs-lookup"><span data-stu-id="42dbf-111">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in.</span></span> <span data-ttu-id="42dbf-112">Если форма открыта в InfoPath, метод **System.Windows.Forms.MessageBox.Show** (который недоступен, когда форма открыта в браузере) используется для отображения окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="42dbf-112">If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="42dbf-113">При создании шаблона формы для в следующем образце кода выберите **пустой** шаблон на вкладке **Создать** в представлении Backstage.</span><span class="sxs-lookup"><span data-stu-id="42dbf-113">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view.</span></span> <span data-ttu-id="42dbf-114">(Кроме того, можно выбрать **Форма веб-браузера** в раскрывающемся списке **тип формы** в разделе категория **Совместимость** диалогового окна **Параметры формы** .) Чтобы обеспечить поддержку класс **MessageBox** , добавьте ссылку на **System.Windows.Forms** на.</span><span class="sxs-lookup"><span data-stu-id="42dbf-114">(Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the .</span></span> <span data-ttu-id="42dbf-115">Вкладка **NET** диалогового окна **Добавить ссылку на** поле в Visual Studio 2012, а затем добавьте директива **using** или **Imports** для **System.Windows.Forms** в разделе объявлений модуля кода формы.</span><span class="sxs-lookup"><span data-stu-id="42dbf-115">**NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
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


