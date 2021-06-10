---
title: Контейнерный объект (DAO)
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
# <a name="container-object-dao"></a>Контейнерный объект (DAO)

**Область применения**: Access 2013, Office 2013

Объект **Контейнера** объединяет аналогичные типы **объектов Document.**

## <a name="remarks"></a>Примечания

Каждый **объект Базы** данных имеет коллекцию **контейнеров,** состоящую из встроенных **контейнерных** объектов. Приложения могут определять собственные типы документов и соответствующие контейнеры (только базы данных баз данных Microsoft Access); однако эти объекты не всегда могут поддерживаться с помощью DAO.

Некоторые из этих **объектов контейнера** определяются механизмом базы данных Microsoft Access, а другие могут быть определены другими приложениями. В следующей таблице перечислены имя каждого объекта **контейнера,** определенного движком базы данных Microsoft Access, и тип информации, которая в нем содержится.

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
<td><p>Сохраненные отношения</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Не путайте **объекты Container,** перечисленные в предыдущей таблице, с коллекциями с одним и тем же именем. Объект Контейнера **баз** данных относится к всем сохраненным объектам базы данных, но коллекция **Баз** данных относится только к объектам баз данных, которые открыты в определенном рабочем пространстве.

Каждый **объект Контейнер** имеет коллекцию **Документов,** содержащую объекты **Document,** описывая экземпляры встроенных объектов типа, указанного **контейнером.** Обычно объект **Container** используется в качестве промежуточной ссылки на сведения в **объекте Document.** Вы также можете использовать коллекцию **Контейнеры,** чтобы установить безопасность для всех объектов **Document** того или иного типа.

С существующим **объектом Контейнер** можно:

- Чтобы **вернуть** заранее задав имя объекта Container, используйте **свойство Name.**

- Используйте свойство **Owner,** чтобы установить или вернуть владельца **объекта Container.** Чтобы установить свойство **Owner,** необходимо иметь разрешение на написание объекта **Container,** а также установить его имя существующего объекта **User** или **Group.**

- Используйте свойства **Permissions** и **UserName** для набора разрешений доступа для **объекта Контейнер;** любой **объект Document,** созданный в коллекции **Документов** объекта **Container,** наследует эти параметры разрешений доступа.

Так **как объекты Container** встроены, нельзя создавать новые объекты **контейнера** или удалять существующие.

Чтобы сослаться на объект **Container** в коллекции по его порядковому номеру или по параметру свойства **Name,** используйте любую из следующих форм синтаксиса:

- **Контейнеры**(0)

- **Контейнеры***("имя")*

- **Контейнеры** \! \[ *имя*\]

## <a name="example"></a>Пример

В этом примере содержится коллекция **контейнеров** базы данных Northwind и коллекция **свойств** каждого объекта **Контейнера** в коллекции.

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
