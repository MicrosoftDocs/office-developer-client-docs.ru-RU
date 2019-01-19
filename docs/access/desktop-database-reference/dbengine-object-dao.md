---
title: Объект DBEngine (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 479eff80d25279a1c5e918a3b639443ad3b25c6c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703687"
---
# <a name="dbengine-object-dao"></a>Объект DBEngine (DAO)

**Область применения**: Access 2013, Office 2013

Объект **DBEngine** — это объект верхнего уровня объектной модели DAO.

## <a name="remarks"></a>Комментарии

Объект **DBEngine** содержит и определяет все прочие объекты в иерархии объектов DAO. Вы не можете создавать дополнительные объекты **DBEngine** и объект **DBEngine** не является частью какой-либо коллекции.

С помощью любого типа базы данных или подключения вы можете:

  - Использовать свойство **Version**для получения номера версии DAO.

  - Используйте свойство **LoginTimeout**, чтобы получить или задать время ожидания входа ODBC, и метод **RegisterDatabase**, чтобы предоставить информацию ODBC ядру СУБД Microsoft Access.

  - Используйте свойства **DefaultPassword** и **DefaultUser**, чтобы настроить идентификация и пароль пользователя для используемого по умолчанию объекта **Workspace**.

  - Используйте метод **CreateWorkspace**, чтобы создать новый объект **Workspace**. Вы можете использовать необязательные аргументы, чтобы переопределять свойства **DefaultType**, **DefaultPassword** и **DefaultUser**.

  - Используйте метод **OpenDatabase**, чтобы открыть базу данных в используемом по умолчанию объекте **Workspace**, и методы **BeginTrans**, **Commit** и **Rollback** для управления транзакциями в используемом по умолчанию объекте **Workspace**.

  - Используйте коллекцию **Workspaces** для ссылки на конкретные объекты **Workspace**.

  - Используйте коллекцию **Errors**, чтобы проверить сведения об ошибке доступа данных.

Другие свойства и методы доступны только при использовании DAO с ядром СУБД Microsoft Access. Можно использовать их для управления ядром СУБД Microsoft Access и его свойствами и выполнения задач на временных объектах, которые не являются элементами коллекции. Например, вы можете:

  - Использовать метод **CreateDatabase**, чтобы создать новый объект **Database** ядра СУБД Microsoft Access.

  - Используйте метод **Idle** для выполнения любой незавершенной задачи с помощью ядра СУБД Microsoft Access.

  - Используйте методы **CompactDatabase** и **RepairDatabase** для сохранения файлов баз данных.

  - Используйте свойства **IniPath** и **SystemDB**, чтобы указать расположение сведений реестра Windows для ядра СУБД Microsoft Access и файла с информацией о рабочей группы Microsoft Access соответственно. Метод **SetOption** позволяет перенастраивать параметры реестра Windows для ядра СУБД Microsoft Access.

После изменения настроек свойств **DefaultType** и **IniPath** только последующие объекты **Workspace** отразят эти изменения.

Чтобы сослаться на коллекцию, которая принадлежит к объекту **DBEngine** или чтобы сослаться на метод или свойство, которое относится к этому объекту, используйте следующий синтаксис:

\[**DBEngine**.\]\[collection | method | property\]

## <a name="example"></a>Пример

В этом примере перечисляется коллекция объекта **DBEngine**.

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
