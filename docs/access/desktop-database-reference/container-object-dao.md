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

Объект **Container** группирует похожие типы объектов **документа** .

## <a name="remarks"></a>Примечания

Каждый объект **базы данных** содержит коллекцию **Containers** , состоящую из встроенных объектов **контейнера** . Приложения могут определять собственные типы документов и соответствующие контейнеры (только базы данных ядра СУБД Microsoft Access); Тем не менее, эти объекты не всегда поддерживаются с помощью DAO.

Некоторые из этих объектов **Container** определены ядром СУБД Microsoft Access, в то время как другие могут определять другие приложения. В следующей таблице приведены имена всех объектов **Container** , определенных ядром СУБД Microsoft Access, и типы данных, которые он содержит.

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
> Не путайте объекты **контейнера** , перечисленные в предыдущей таблице, с коллекциями с одинаковыми именами. Объект **контейнера** баз данных относится ко всем сохраненным объектам базы данных, но семейство **баз данных** относится только к объектам базы данных, открытым в определенной рабочей области.

Каждый объект **Container** содержит коллекцию **Documents** , содержащую объекты **Document** , которые описывают экземпляры встроенных объектов типа, указанного в **контейнере**. Как правило, объект **Container** используется в качестве промежуточной ссылки на информацию в объекте **Document** . Вы также можете использовать коллекцию **Containers** , чтобы задать безопасность для всех объектов **документа** определенного типа.

С помощью существующего объекта **Container** можно выполнить следующие действия:

- Используйте свойство **Name** , чтобы возвратить предварительно определенное имя объекта **Container** .

- Используйте свойство **owner** , чтобы задать или вернуть владельца объекта **Container** . Чтобы задать свойство **owner** , необходимо иметь разрешение на запись для объекта **Container** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .

- Используйте свойства **Permissions** и **username** , чтобы задать разрешения доступа для объекта **Container** ; любой объект **документа** , созданный в коллекции **Documents** объекта **Container** , наследует эти параметры разрешений на доступ.

Так как объекты **контейнеров** являются встроенными, вы не можете создавать новые объекты- **контейнеры** или удалять существующие.

Чтобы сослаться на объект **контейнера** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:

- **Контейнеры**(0)

- **Контейнеры**("*имя*")

- **Containers**\!\[*Имя* контейнера\]

## <a name="example"></a>Пример

В этом примере показано, как перечислить коллекцию **контейнеров** базы данных Northwind и коллекцию **свойств** каждого объекта **Container** в коллекции.

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
