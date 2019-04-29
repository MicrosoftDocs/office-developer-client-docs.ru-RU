---
title: Доступ к данным приложения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- имена приложений [InfoPath 2007], доступ к имени приложения [InfoPath 2007], InfoPath 2007, доступ к данным приложения, доступ к версии приложения [InfoPath 2007], версии приложения [InfoPath 2007], идентификаторы языков [InfoPath 2007], LCID [InfoPath 2007], данные приложения [InfoPath 2007], доступ к ИДЕНТИФИКАТОРу языка [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Объектная модель управляемого кода InfoPath предоставляет объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, включая информацию, связанную с базовым XML-документом формы и файлом определения формы (XSF-файлом). Доступ к этим данным осуществляется через объект верхнего уровня в иерархии объектной модели InfoPath, экземпляр которого создается с помощью класса Application.
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417233"
---
# <a name="access-application-data"></a><span data-ttu-id="b82bd-105">Доступ к данным приложения</span><span class="sxs-lookup"><span data-stu-id="b82bd-105">Access Application Data</span></span>

<span data-ttu-id="b82bd-106">Объектная модель управляемого кода InfoPath предоставляет объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, включая информацию, связанную с базовым XML-документом формы и файлом определения формы (XSF-файлом).</span><span class="sxs-lookup"><span data-stu-id="b82bd-106">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="b82bd-107">Доступ к этим данным осуществляется через объект верхнего уровня в иерархии объектной модели InfoPath, экземпляр которого создается с помощью класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b82bd-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="b82bd-108">В проекте шаблона формы с управляемым кодом InfoPath, созданном с помощью Visual Studio 2012, можно использовать ключевое слово **this** (C#) или **Me** (Visual Basic) для доступа к экземпляру класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , представляющего текущее приложение InfoPath. который затем можно использовать для доступа к свойствам и методам класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b82bd-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b82bd-109">Пример</span><span class="sxs-lookup"><span data-stu-id="b82bd-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="b82bd-110">Отображение имени, версии и идентификатора языка приложения</span><span class="sxs-lookup"><span data-stu-id="b82bd-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="b82bd-111">В следующем примере свойства [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) и [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) используются для возврата имени и номера версии запущенного экземпляра InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b82bd-111">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="b82bd-112">Затем свойство [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) используется для возвращения объекта **LanguageSettings** , который, в свою очередь, используется для возврата LCID (четырехзначное число) для языка, который в данный момент используется для языка пользовательского интерфейса InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b82bd-112">The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language.</span></span> <span data-ttu-id="b82bd-113">И наконец, вся эта информация отображается в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="b82bd-113">Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b82bd-114">Чтобы свойство **LanguageSettings** работало, необходимо установить ссылку на библиотеку объектов Microsoft Office 14,0 на вкладке **com** диалогового окна " **Добавление ссылки** " в Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="b82bd-114">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> <span data-ttu-id="b82bd-115">При этом будет указана ссылка на пространство имен **Microsoft.Office.Core**, содержащее класс **LanguageSettings**.</span><span class="sxs-lookup"><span data-stu-id="b82bd-115">This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class.</span></span> <span data-ttu-id="b82bd-116">Кроме того, форму необходимо запускать с полным доверием.</span><span class="sxs-lookup"><span data-stu-id="b82bd-116">Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="b82bd-117">В этом примере требуется директива **using** или **Imports** для пространства имен **Microsoft.Office.Core** в разделе объявлений модуля кода формы.</span><span class="sxs-lookup"><span data-stu-id="b82bd-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


