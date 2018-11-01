---
title: DBEngine Object (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86c14ef0e9443965b2e80af329d4cca6023d1467
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873634"
---
# <a name="dbengine-object-dao"></a>DBEngine Object (DAO)

**Применимо к**: Access 2013, Office 2013

Объект **DBEngine** — это объект верхнего уровня в объектной модели DAO.

## <a name="remarks"></a>Замечания

Объект **DBEngine** содержит и управляет все объекты в иерархии объектов DAO. Не удается создать дополнительные объекты **DBEngine** и **DBEngine** объект не является элемент все семейства сайтов.

Любой тип базы данных или подключения можно выполнить следующие действия.

  - Используйте свойство **Version** для получения номера версии DAO.

  - Используйте свойство **LoginTimeout** получить или задать время ожидания входа ODBC, а метод **RegisterDatabase** для предоставления сведений ODBC к ядру базы данных Microsoft Access.

  - Используйте **DefaultPassword** и **DefaultUser** свойства, чтобы задать идентификатор пользователя и пароль для объекта **рабочей области** по умолчанию.

  - Используйте метод **CreateWorkspace** для создания нового объекта **рабочей области** . Дополнительные аргументы, которые можно использовать для переопределения параметров свойства **DefaultType**, **DefaultPassword**и **DefaultUser** .

  - Метод **OpenDatabase** используется для открытия базы данных в **рабочей области**по умолчанию и использовать **BeginTrans**, **завершения**и **отката** методы для управления транзакции в **рабочую область**по умолчанию.

  - Используйте коллекцию **рабочих областей** для ссылок на объекты, определенные **рабочей области** .

  - Используйте коллекцию **ошибок** для просмотра сведений об ошибках доступа к данным.

Другие свойства и методы доступны только при использовании DAO ядро базы данных Microsoft Access. Можно использовать их для управления ядро базы данных Microsoft Access, изменить его свойства и выполнять задачи с временные объекты, не являющиеся частью коллекции. Например можно выполнить следующие действия.

  - Метод **CreateDatabase** используется для создания нового объекта **базы данных** ядра базы данных Microsoft Access.

  - Используйте метод **Idle** для включения ядро базы данных Microsoft Access завершить все ожидающие задачи.

  - Используйте методы **CompactDatabase** и **RepairDatabase** для сохранения файлов базы данных.

  - Используйте **IniPath** и **SystemDB** свойства, чтобы указать расположение ядро СУБД Microsoft Access сведений реестра Windows и файл рабочей группы Microsoft Access, соответственно. Метод **SetOption** позволяет переопределить параметры реестра windows для ядро базы данных Microsoft Access.

После изменения параметров свойства **DefaultType** и **IniPath** эти изменения будут отражены в последующих объектов **рабочей области** .

Чтобы указать коллекцию параметров, к которой принадлежит объект **DBEngine** или ссылаться на метод или свойство, которое применяется для данного объекта, используйте следующий синтаксис:

\[**DBEngine**. \] \[коллекции | метод | Свойство\]

## <a name="example"></a>Пример

В этом примере перечисляются коллекций объектов **DBEngine** .

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
