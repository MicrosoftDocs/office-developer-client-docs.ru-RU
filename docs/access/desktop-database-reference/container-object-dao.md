---
title: Объект Container (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295634"
---
# <a name="container-object-dao"></a>Объект Container (DAO)

**Область применения**: Access 2013, Office 2013

Объект **контейнера** объединяет похожие типы **объектов Document.**

## <a name="remarks"></a>Заметки

Каждый **объект Database** имеет коллекцию **контейнеров,** состоящую из встроенных **объектов-контейнеров.** Приложения могут определять собственные типы документов и соответствующие контейнеры (только для баз данных ям баз данных Microsoft Access); однако эти объекты не всегда поддерживаются с помощью DAO.

Некоторые из этих **объектов-контейнеров** определяются механизмом баз данных Microsoft Access, а другие — другими приложениями. В следующей таблице перечислены имена каждого объекта **Container,** определяемого яном базы данных Microsoft Access, и тип информации, которую он содержит.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя контейнера</p></th>
<th><p>Содержит сведения о</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Databases</p></td>
<td><p>Сохраненные базы данных</p></td>
</tr>
<tr class="even">
<td><p>Таблицы</p></td>
<td><p>Сохраненные таблицы и запросы</p></td>
</tr>
<tr class="odd">
<td><p>Relations</p></td>
<td><p>Сохраненные связи</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Не путайте **объекты-контейнеры,** перечисленные в предыдущей таблице, с коллекциями с тем же именем. Объект **контейнера databases** ссылается на все сохраненные объекты базы данных, но коллекция **Databases** ссылается только на объекты баз данных, открытые в определенной рабочей области.

Каждый **объект** Container имеет коллекцию **Documents,** содержащую объекты **Document,** которые описывают экземпляры встроенных объектов типа, указанного **контейнером.** Обычно объект-контейнер  используется в качестве промежуточной ссылки на сведения в **объекте Document.** Вы также можете использовать коллекцию **Containers,** чтобы установить безопасность для всех объектов **Document** заданного типа.

С помощью существующего **объекта Container** можно:

- Используйте свойство **Name** для возврата предопределенного имени объекта **Container.**

- Используйте свойство **Owner,** чтобы установить или вернуть владельца объекта **Container.** Чтобы установить свойство **Owner,** необходимо иметь разрешение на написание для объекта **Container,** а также установить для свойства имя существующего объекта **User** или **Group.**

- Используйте свойства **Permissions** и **UserName,** чтобы установить разрешения доступа для **объекта Container;** Любой **объект Document,** созданный в коллекции **Documents** объекта **Container,** наследует эти параметры разрешений доступа.

Поскольку  объекты-контейнеры являются встроенными, нельзя создавать новые **объекты-контейнеры** или удалять существующие.

Чтобы сослаться на объект **контейнера** в коллекции по его порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис форм:

- **Контейнеры**(0)

- **Containers**("*name*")

- **Контейнеры** \! \[ *name*\]

## <a name="example"></a>Пример

В этом примере включается enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
