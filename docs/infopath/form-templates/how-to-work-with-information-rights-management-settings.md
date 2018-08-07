---
title: Работа с параметрами управления правами на доступ к данным
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Управление правами на доступ [infopath 2007] InfoPath 2007, управление правами на к данным [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: 'Существует два типа параметров управления правами на доступ к данным (IRM) в Microsoft InfoPath: одна для защиты доступа к шаблонам форм InfoPath, а другая — для контроля доступа к и действий в виде данные, содержащиеся в заполненные формы.'
ms.openlocfilehash: 4e6fdac6a0b2b5cd6a29de948cc9dbbd01a407d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807529"
---
# <a name="work-with-information-rights-management-settings"></a>Работа с параметрами управления правами на доступ к данным

Существует два типа параметров управления правами на доступ к данным (IRM) в Microsoft InfoPath: одна для защиты доступа к шаблонам форм InfoPath, а другая — для контроля доступа к и действий в виде данные, содержащиеся в заполненные формы.
  
> [!NOTE]
> Ограничение разрешений доступно только для шаблонов форм, совместимых с редактором InfoPath. Шаблоны форм, совместимые с веб-браузером, не поддерживают управление правами на доступ к данным. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Добавление команды "Управление учетными данными" на панель быстрого доступа

Команда **Управление учетными данными**, которая использовалась для работы с параметрами управления правами на доступ к данным при разработке шаблона формы, теперь недоступна по умолчанию. Чтобы добавить ее на **Панель быстрого доступа**, выполните следующие операции.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Добавление команды "Управление учетными данными" на панель быстрого доступа

1.   Щелкните стрелку в правом углу **Панели быстрого доступа** для вызова меню **Настройка панели быстрого доступа**, а затем выберите **Другие команды**.
    
2. В списке **Выбрать команды из** выберите **Все команды**.
    
3. Пролистайте список вниз до раздела **Управление учетными данными**, а затем нажмите кнопку **Добавить**.
    
4. Нажмите кнопку **ОК**.
    
Дополнительные сведения об использовании команды **Управление учетными данными** и диалогового окна **Разрешения** в InfoPath см. в разделе "Создание шаблона формы с ограниченными разрешениями" справки по InfoPath. 
  
## <a name="the-irm-object-model"></a>Объектная модель управления правами на доступ к данным

Используйте класс [разрешения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) для доступа к [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) и IRM параметры разрешений, которые можно применить к форме. Для доступа к объекту **разрешений** , связанного с шаблоном формы, используйте свойство [разрешение](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Возвращаемый объект **разрешения** предоставляет доступ к коллекцию объектов [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) , связанный с шаблоном формы и каждого экземпляра формы, созданные с помощью этого шаблона. 
  
Объект **разрешения** и его свойствам и методам, доступны ли разрешения не имеют полномочий на шаблоне активной формы или нет. Используйте свойство [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) для определения, является ли формы с ограниченными разрешениями. 
  
Ниже перечислены способы включения разрешений для формы с помощью свойств и методов класса "Permission".
  
Для свойства **Enabled** задается значение **true**.
  
Свойство [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) имеет значение. 
  
Свойство [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) имеет значение. 
  
Для свойства [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) значение **true** или **false**.
  
Метод [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) вызывается. 
  
> [!NOTE]
> Если на компьютере пользователя не установлен клиент управления правами Windows, то использование класса **Permission** приводит к появлению исключения. 
  
Для программной работы с параметрами управления правами на доступ к данным для отдельных пользователей в формах используйте классы **UserPermissionCollection** и **UserPermission**. 
  
Объект **UserPermission** связывает набор разрешений для текущей формы с одним пользователем и датой истечения срока действия необязательно. Используйте метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) класса **UserPermissionCollection** для добавления и предоставление пользователю набор разрешений для текущей формы. Используйте метод [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) класса **UserPermissionCollection** для удаления пользователя и разрешения пользователя. Хотя некоторые разрешения, предоставленные через пользовательский интерфейс применяются ко всем пользователям, например печати и окончания срока действия, можно использовать классы **UserPermissionCollection** и **UserPermission** для назначения их на основе пользователя с уровня пользователя даты окончания срока действия. Объектная модель разработчики перечисление параметры разрешений в форме и предоставляют функциональные возможности, позволяющие пользователям формы для добавления разрешений к форме без использования области задач **Разрешение форма** или диалоговое окно **разрешения** . 
  
> [!NOTE]
> Разрешения нельзя применить, если форма находится в режиме просмотра. Поэтому все свойства класса **Permission** при просмотре формы доступны только для чтения. В режиме просмотра свойство **Enabled** всегда возвращает значение **false**, а при попытке кода изменить это значение возникает исключение **System.Runtime.InteropServices.COMException** и возвращается ошибка "Свойство/метод недоступны в режиме предварительного просмотра". Аналогичным образом методы, связанные с классами **UserPermission** и **UserPermissionCollection**, также будут возвращать это сообщение об ошибке при использовании в режиме просмотра. 
  
### <a name="overview-of-the-permission-class"></a>Обзор класса "Permission"

Класс **UserPermissionCollection** предоставляет указанные ниже свойства и один метод. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx)  <br/> |Применяет к форме политику с помощью файла шаблона политики.  <br/> |
|Свойство [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx)  <br/> |Возвращает или задает автора текущей формы как адрес электронной почты.  <br/> |
|Свойство [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx)  <br/> |Возвращает или задает значение, указывающее, включены ли для текущей формы параметры разрешений, представленные объектом **Permission**.  <br/> |
|Свойство [PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx)  <br/> |Возвращает или задает значение, указывающее, применяется ли политика разрешений к текущей форме.  <br/> |
|Свойство [PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx)  <br/> |Возвращает описание политики, примененной к текущей форме.   <br/> |
|Свойство [PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx)  <br/> |Возвращает имя политики, примененной к текущей форме.  <br/> |
|Свойство [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx)  <br/> |Получает или задает файл, URL-адрес или адрес электронной почты для связи для пользователей, которым требуются дополнительные разрешения для текущей формы.  <br/> |
|Для свойства [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx)  <br/> |Возвращает или задает значение, указывающее, следует ли кэшировать лицензию пользователя на просмотр текущей формы для обеспечения автономного просмотра в том случае, если пользователь не может подключиться к серверу управления правами.   <br/> |
|Свойство [Разрешенияпользователя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx)  <br/> |Возвращает объект **UserPermissionCollection** для текущей формы.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Обзор класса "UserPermissionCollection"

Класс **UserPermissionCollection** предоставляет следующие свойства и методы. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) (+ 3 перегрузки)  <br/> |Добавляет нового пользователя для текущей формы с указанием разрешений и срока действия (необязательно).  <br/> |
|Метод [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)  <br/> |Удаляет из коллекции объект **UserPermission** с указанным идентификатором **UserId**.  <br/> |
|Метод [RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx)  <br/> |Удаляет из коллекции все объекты **UserPermission**.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)  <br/> |Возвращает количество объектов **UserPermission** в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) (+ 1 перегрузка)  <br/> |Возвращает объект **UserPermission**.  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Обзор класса "UserPermission"

Класс **UserPermission** предоставляет указанные ниже свойства и один метод. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)  <br/> |Удаляет текущий объект **UserPermission** из разрешений формы.  <br/> |
|Свойство [ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx)  <br/> |Возвращает или задает необязательный срок действия разрешений текущей формы, назначенных пользователю, связанному с экземпляром класса **UserPermission**.  <br/> |
|Свойство [разрешения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx)  <br/> |Возвращает или задает значение, представляющее разрешения текущей формы, назначенные пользователю, связанному с экземпляром класса **UserPermission**.   <br/> |
|Свойство [UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx)  <br/> |Получает адрес электронной почты пользователя, разрешения которого на текущую форму определяются указанным объектом **UserPermission** .  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>Перечисление "PermissionType"

Разрешения пользователей изменять или с помощью значений перечисления [PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) . 
  
|**Имя**|**Описание**|
|:-----|:-----|
|**PermissionType.Change** <br/> |Позволяет пользователям просматривать, редактировать, копировать и сохранять, но не печатать форму. Эквивалентно совмещению разрешений **Read**, **Edit**, **Save** и **Extract**.<br/> |
|**PermissionType.Edit** <br/> |Позволяет пользователю редактировать форму.  <br/> |
|**PermissionType.Extract** <br/> |Позволяет пользователю с разрешением **Read** копировать содержимое в форме.  <br/> |
|**PermissionType.FullControl** <br/> |Позволяет пользователю добавлять, изменять и удалять разрешения других пользователей формы.  <br/> |
|**PermissionType.ObjectModel** <br/> |Позволяет пользователю обращаться к документу формы программным способом через его объектную модель. Пользователи, не имеющие разрешения **ObjectModel**, не могут использовать объектную модель для определения их собственных разрешений.<br/> |
|**PermissionType.Print** <br/> |Позволяет пользователю печатать форму.  <br/> |
|**PermissionType.Read** <br/> |Позволяет пользователю читать (просматривать) форму. (Разрешения **Read** и **View** эквивалентны.)<br/> |
|**PermissionType.Save** <br/> |Позволяет пользователю сохранять форму.  <br/> |
|**PermissionType.View** <br/> |Позволяет пользователю просматривать (считывать) форму (эквивалентно разрешениям **Read** и **View**). <br/> |
   
### <a name="example"></a>Пример

В следующем примере при нажатии элемента управления **Кнопка** выполняется получение объекта **UserPermissionsCollection** для текущей формы, добавление уровня разрешений "Изменение доступа" для пользователя и задание срока действия, который составляет два дня от текущей даты. 
  
```cs
public void CTRL1_Clicked(object sender, ClickedEventArgs e)
{
   string strExpirationDate = DateTime.Today.AddDays(2).ToString();
   DateTime dtExpirationDate = DateTime.Parse(strExpirationDate);
   this.Permission.UserPermissions.Add("someone@example.com", 
      PermissionType.Change, dtExpirationDate);
}
```

```vb
Public Sub CTRL1_Clicked(ByVal sender As Object, _
   ByVal e As ClickedEventArgs)
   Dim strExpirationDate As String = _
      DateTime.Today.AddDays(2).ToString()
   dtExpirationDate As DateTime = DateTime.Parse(strExpirationDate)
   Me.Permission.UserPermissions.Add("someone@example.com", _
      PermissionType.Change, dtExpirationDate)
End Sub
```


