---
title: Доступ к данным приложений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- имена приложений [infopath 2007], доступ к имени приложения [InfoPath 2007], InfoPath 2007, доступ к данным приложений, доступ к версии приложения [InfoPath 2007], версии приложений [InfoPath 2007], языковые ID [InfoPath 2007],LCID [InfoPath 2007], данные приложений [InfoPath 2007], доступ к языковой ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Объектная модель управляемого кода InfoPath предоставляет объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, включая информацию, связанную с базовым XML-документом формы и файлом определения формы (XSF-файлом). Эти данные можно получить через объект верхнего уровня в иерархии объектной модели InfoPath, который мгновенно используется с помощью класса Application.
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417233"
---
# <a name="access-application-data"></a>Доступ к данным приложений

Объектная модель управляемого кода InfoPath предоставляет объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, включая информацию, связанную с базовым XML-документом формы и файлом определения формы (XSF-файлом). Эти данные можно получить через объект верхнего уровня в иерархии объектной модели InfoPath, который мгновенно используется с помощью [класса Application.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) 
  
В проекте шаблона управляемых форм кода InfoPath, созданном с Visual Studio 2012 г., можно использовать это **ключевое** слово [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) (C#) или Me **(Visual Basic)** для доступа к экземпляру класса Приложения, представляю которому является текущее приложение InfoPath, которое затем можно использовать для доступа к свойствам и методам класса [Приложения.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) 
  
## <a name="example"></a>Пример

### <a name="displaying-the-application-name-version-and-language-id"></a>Отображение имени, версии и идентификатора языка приложения

В следующем примере свойства [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) и [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) используются для возврата имени и номера версии запущенного экземпляра InfoPath. Затем [свойство LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) используется для возврата объекта **LanguageSettings,** который, в свою очередь, используется для возврата LCID (четырехзначного номера) для языка, который в настоящее время используется для языка пользовательского интерфейса InfoPath. И наконец, вся эта информация отображается в окне сообщения. 
  
> [!IMPORTANT]
> Чтобы свойство **LanguageSettings** работало, необходимо установить ссылку на объектную библиотеку Microsoft Office 14.0 из вкладки **COM** диалогового окна **Add Reference** в Visual Studio 2012 г. При этом будет указана ссылка на пространство имен **Microsoft.Office.Core**, содержащее класс **LanguageSettings**. Кроме того, форму необходимо запускать с полным доверием. 
  
В этом примере требуется директива **using** или **Imports** для пространства имен **Microsoft.Office.Core** в разделе объявлений модуля кода формы. 
  
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


