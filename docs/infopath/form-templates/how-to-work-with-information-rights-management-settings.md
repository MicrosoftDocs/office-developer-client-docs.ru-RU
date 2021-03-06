---
title: Работа с управлением правами на информацию Параметры
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- управление правами на информацию [infopath 2007], InfoPath 2007, Управление правами на информацию,IRM [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: 'В Microsoft InfoPath доступны два типа параметров управления правами на информацию ( IRM): один для защиты доступа к шаблонам форм InfoPath и один для контроля доступа к данным форм и действий, содержащихся в завершенных формах.'
ms.openlocfilehash: 6f7317cfdc4e6bfc89482e813b1670c8b8861a6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420012"
---
# <a name="work-with-information-rights-management-settings"></a>Работа с управлением правами на информацию Параметры

В Microsoft InfoPath доступны два типа параметров управления правами на информацию ( IRM): один для защиты доступа к шаблонам форм InfoPath и один для контроля доступа к данным форм и действий, содержащихся в завершенных формах.
  
> [!NOTE]
> Ограничение разрешений доступно только для шаблонов форм, совместимых с редактором InfoPath. Шаблоны форм, совместимые с веб-браузером, не поддерживают управление правами на доступ к данным. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Добавление команды "Управление учетными данными" на панель быстрого доступа

Команда **Управление учетными данными**, которая использовалась для работы с параметрами управления правами на доступ к данным при разработке шаблона формы, теперь недоступна по умолчанию. Чтобы добавить ее на **Панель быстрого доступа**, выполните следующие операции.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Добавление команды "Управление учетными данными" на панель быстрого доступа

1.  Щелкните стрелку в правом углу **Панели быстрого доступа** для вызова меню **Настройка панели быстрого доступа**, а затем выберите **Другие команды**.
    
2. В списке **Выбрать команды из** выберите **Все команды**.
    
3. Пролистайте список вниз до раздела **Управление учетными данными**, а затем нажмите кнопку **Добавить**.
    
4. Нажмите кнопку **ОК**.
    
Дополнительные сведения об использовании команды **Управление учетными данными** и диалогового окна **Разрешения** в InfoPath см. в разделе "Создание шаблона формы с ограниченными разрешениями" справки по InfoPath. 
  
## <a name="the-irm-object-model"></a>Объектная модель управления правами на доступ к данным

Используйте класс [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) для доступа к настройкам [разрешений UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) и IRM, которые можно применить к форме. Чтобы получить доступ **к объекту Permission,** связанному с шаблоном формы, используйте свойство [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Объект returned **Permission** предоставляет доступ к коллекции объектов [UserPermission,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) связанных с шаблоном формы, и к каждому экземпляру формы, созданному с этим шаблоном. 
  
Объект **Permission** и его свойства и методы доступны в зависимости от наличия ограничений разрешений для активного шаблона формы. Используйте свойство [Включено,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) чтобы определить, имеет ли форма ограничения разрешений. 
  
Ниже перечислены способы включения разрешений для формы с помощью свойств и методов класса "Permission".
  
Для свойства **Enabled** задается значение **true**.
  
Свойство [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) установлено. 
  
Свойство [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) установлено. 
  
Свойство [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) задано для true **или** **false**.
  
Называется [метод ApplyPolicy.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) 
  
> [!NOTE]
> Если на компьютере пользователя не установлен клиент управления правами Windows, то использование класса **Permission** приводит к появлению исключения. 
  
Для программной работы с параметрами управления правами на доступ к данным для отдельных пользователей в формах используйте классы **UserPermissionCollection** и **UserPermission**. 
  
Объект **UserPermission** связывает набор разрешений для текущей формы с отдельным пользователем и задает срок действия (необязательно). Используйте метод [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) класса **UserPermissionCollection,** чтобы добавить и предоставить пользователю набор разрешений в текущей форме. Чтобы [удалить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) разрешения пользователя и пользователя, используйте метод Remove класса **UserPermissionCollection.** Хотя некоторые разрешения, предоставляемые через интерфейс пользователя, например для печати и срока действия, применяются ко всем пользователям, можно воспользоваться классами **UserPermission** и **UserPermissionCollection** для назначения их отдельным пользователям с индивидуальными сроками действия. Объектная модель позволяет разработчикам выполнять перечисление параметров разрешений в форме и предоставлять возможности, позволяющие пользователям формы добавлять в форму разрешения без использования области задач **Разрешения для формы** или диалогового окна **Разрешения**. 
  
> [!NOTE]
> Разрешения нельзя применить, если форма находится в режиме просмотра. Поэтому все свойства класса **Permission** при просмотре формы доступны только для чтения. В режиме просмотра свойство **Enabled** всегда возвращает значение **false**, а при попытке кода изменить это значение возникает исключение **System.Runtime.InteropServices.COMException** и возвращается ошибка "Свойство/метод недоступны в режиме предварительного просмотра". Аналогичным образом методы, связанные с классами **UserPermission** и **UserPermissionCollection**, также будут возвращать это сообщение об ошибке при использовании в режиме просмотра. 
  
### <a name="overview-of-the-permission-class"></a>Обзор класса "Permission"

Класс **UserPermissionCollection** предоставляет указанные ниже свойства и один метод. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Метод ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx)  <br/> |Применяет к форме политику с помощью файла шаблона политики.  <br/> |
|[Свойство DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx)  <br/> |Получает или задает автора текущей формы в качестве адреса электронной почты.  <br/> |
|[Свойство Включено](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx)  <br/> |Возвращает или задает значение, указывающее, включены ли для текущей формы параметры разрешений, представленные объектом **Permission**.  <br/> |
|[Свойство PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx)  <br/> |Возвращает или задает значение, указывающее, применяется ли политика разрешений к текущей форме.  <br/> |
|[Свойство PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx)  <br/> |Возвращает описание политики, примененной к текущей форме.  <br/> |
|[Свойство PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx)  <br/> |Возвращает имя политики, примененной к текущей форме.  <br/> |
|[Свойство RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx)  <br/> |Получает или задает файл, URL-адрес или адрес электронной почты, чтобы связаться с пользователями, которым необходимы дополнительные разрешения в текущей форме.  <br/> |
|[Свойство StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx)  <br/> |Возвращает или задает значение, указывающее, следует ли кэшировать лицензию пользователя на просмотр текущей формы для обеспечения автономного просмотра в том случае, если пользователь не может подключиться к серверу управления правами.  <br/> |
|[Свойство UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx)  <br/> |Возвращает объект **UserPermissionCollection** для текущей формы.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Обзор класса "UserPermissionCollection"

Класс **UserPermissionCollection** предоставляет следующие свойства и методы. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Добавление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) метода (+3 перегрузки)  <br/> |Добавляет нового пользователя для текущей формы с указанием разрешений и срока действия (необязательно).  <br/> |
|Метод [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)  <br/> |Удаляет из коллекции объект **UserPermission** с указанным идентификатором **UserId**.  <br/> |
|[Метод RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx)  <br/> |Удаляет из коллекции все объекты **UserPermission**.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)  <br/> |Возвращает количество объектов **UserPermission** в коллекции.  <br/> |
|[Свойство Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) (+1 перегрузка)  <br/> |Возвращает объект **UserPermission**.  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Обзор класса "UserPermission"

Класс **UserPermission** предоставляет указанные ниже свойства и один метод. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)  <br/> |Удаляет текущий объект **UserPermission** из разрешений формы.  <br/> |
|[Свойство ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx)  <br/> |Возвращает или задает необязательный срок действия разрешений текущей формы, назначенных пользователю, связанному с экземпляром класса **UserPermission**.  <br/> |
|[Свойство Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx)  <br/> |Возвращает или задает значение, представляющее разрешения текущей формы, назначенные пользователю, связанному с экземпляром класса **UserPermission**.  <br/> |
|[Свойство UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx)  <br/> |Получает адрес электронной почты пользователя, разрешения которого в текущей форме определяются указанным объектом **UserPermission.**  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>Перечисление "PermissionType"

Разрешения пользователя устанавливаются или читаются с помощью значений переумеления [PermissionType.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) 
  
|**Имя**|**Описание**|
|:-----|:-----|
|**PermissionType.Change** <br/> |Позволяет пользователям просматривать, редактировать, копировать и сохранять форму, но не печатать ее. Эквивалентно сочетанию разрешений **Read**, **Edit**, **Save** и **Extract**.<br/> |
|**PermissionType.Edit** <br/> |Позволяет пользователю редактировать форму.  <br/> |
|**PermissionType.Extract** <br/> |Позволяет пользователю с разрешением **Read** копировать содержимое формы.  <br/> |
|**PermissionType.FullControl** <br/> |Позволяет пользователю добавлять, изменять и удалять разрешения для других пользователей формы.  <br/> |
|**PermissionType.ObjectModel** <br/> |Предоставляет пользователю программный доступ к документу формы через его объектную модель. Пользователи без разрешения **ObjectModel** не могут использовать объектную модель для определения собственных разрешений.<br/> |
|**PermissionType.Print** <br/> |Позволяет пользователю печатать форму.  <br/> |
|**PermissionType.Read** <br/> |Позволяет пользователю считывать (просматривать) форму (эквивалентно разрешениям **Read** и **View**).<br/> |
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


