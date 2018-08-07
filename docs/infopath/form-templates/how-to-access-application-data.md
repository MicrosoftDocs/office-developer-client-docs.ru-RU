---
title: Доступ к данным приложения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- имена приложений [infopath 2007], доступ к имени приложения [InfoPath 2007], InfoPath 2007, доступ к данным приложения, доступ к версии приложения [InfoPath 2007], версии приложений [InfoPath 2007], код языка идентификаторы [InfoPath 2007], [InfoPath 2007] данные приложения [InfoPath 2007], доступ к языковой идентификатор [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: InfoPath в объектной модели управляемого кода представлены объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, а также приведены сведения, относящиеся к XML-документом формы и файла определения формы (XSF). Эти данные осуществляется с помощью объекта верхнего уровня в иерархии модели объектов InfoPath, который создается с помощью класса приложения.
ms.openlocfilehash: 3c3f6be4e90e292eb572da836bca0a8dcf1883cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807476"
---
# <a name="access-application-data"></a><span data-ttu-id="d0df9-105">Доступ к данным приложения</span><span class="sxs-lookup"><span data-stu-id="d0df9-105">Access Application Data</span></span>

<span data-ttu-id="d0df9-106">InfoPath в объектной модели управляемого кода представлены объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, а также приведены сведения, относящиеся к XML-документом формы и файла определения формы (XSF).</span><span class="sxs-lookup"><span data-stu-id="d0df9-106">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="d0df9-107">Эти данные осуществляется с помощью объекта верхнего уровня в иерархии модели объектов InfoPath, который создается с помощью класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d0df9-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="d0df9-108">В InfoPath управляемого кода в проект шаблона формы созданы с помощью Visual Studio 2012 можно использовать **Этот** (C#) или ключевое слово **Me** (Visual Basic) для доступа к экземпляру класс [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , который представляет текущего приложения InfoPath Нажмите, который можно использовать для доступа к свойствам и методам класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d0df9-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d0df9-109">Пример</span><span class="sxs-lookup"><span data-stu-id="d0df9-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="d0df9-110">Отображение имени, версии и идентификатора языка приложения</span><span class="sxs-lookup"><span data-stu-id="d0df9-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="d0df9-111">В следующем примере свойства [имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) и [версию](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) используются для возврата имя и номер версии выполняемый экземпляр InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d0df9-111">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="d0df9-112">Свойство [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) затем используется для возврата объекта **LanguageSettings** , который в свою очередь используется для возврата LCID (4 значное число) для языка, который в данный момент используется для язык интерфейса пользователя InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d0df9-112">The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language.</span></span> <span data-ttu-id="d0df9-113">И, наконец вся эта информация отображается в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0df9-113">Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d0df9-114">Для свойства **LanguageSettings** для работы необходимо установить ссылку на библиотеку объектов Microsoft Office 14.0 на вкладке **COM** диалогового окна **Добавить ссылку** в Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="d0df9-114">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> <span data-ttu-id="d0df9-115">Это будет установки ссылки на пространства имен **Microsoft.Office.Core** , который содержит класс **LanguageSettings** .</span><span class="sxs-lookup"><span data-stu-id="d0df9-115">This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class.</span></span> <span data-ttu-id="d0df9-116">Кроме того форма должна быть запущена как полное доверие.</span><span class="sxs-lookup"><span data-stu-id="d0df9-116">Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="d0df9-117">В этом примере требуется директива **using** или **Imports** для пространства имен **Microsoft.Office.Core** в разделе объявлений модуля кода формы.</span><span class="sxs-lookup"><span data-stu-id="d0df9-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
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


