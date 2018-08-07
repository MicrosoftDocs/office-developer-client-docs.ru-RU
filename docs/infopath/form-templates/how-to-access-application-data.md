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
# <a name="access-application-data"></a>Доступ к данным приложения

InfoPath в объектной модели управляемого кода представлены объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, а также приведены сведения, относящиеся к XML-документом формы и файла определения формы (XSF). Эти данные осуществляется с помощью объекта верхнего уровня в иерархии модели объектов InfoPath, который создается с помощью класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
В InfoPath управляемого кода в проект шаблона формы созданы с помощью Visual Studio 2012 можно использовать **Этот** (C#) или ключевое слово **Me** (Visual Basic) для доступа к экземпляру класс [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) , который представляет текущего приложения InfoPath Нажмите, который можно использовать для доступа к свойствам и методам класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
## <a name="example"></a>Пример

### <a name="displaying-the-application-name-version-and-language-id"></a>Отображение имени, версии и идентификатора языка приложения

В следующем примере свойства [имя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) и [версию](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) используются для возврата имя и номер версии выполняемый экземпляр InfoPath. Свойство [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) затем используется для возврата объекта **LanguageSettings** , который в свою очередь используется для возврата LCID (4 значное число) для языка, который в данный момент используется для язык интерфейса пользователя InfoPath. И, наконец вся эта информация отображается в окне сообщения. 
  
> [!IMPORTANT]
> Для свойства **LanguageSettings** для работы необходимо установить ссылку на библиотеку объектов Microsoft Office 14.0 на вкладке **COM** диалогового окна **Добавить ссылку** в Visual Studio 2012. Это будет установки ссылки на пространства имен **Microsoft.Office.Core** , который содержит класс **LanguageSettings** . Кроме того форма должна быть запущена как полное доверие. 
  
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


