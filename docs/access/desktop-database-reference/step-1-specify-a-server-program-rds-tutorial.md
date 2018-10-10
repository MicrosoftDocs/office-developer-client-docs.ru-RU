---
title: 'Step 1: Specify a Server Program (RDS Tutorial)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89aa87aa63a3d8bfdeb291f78d6525f51c4262b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479740"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a>Step 1: Specify a Server Program (RDS Tutorial)


**Применимо к**: Access 2013 | Office 2013

В общем случае используйте [RDS. Пространства данных](dataspace-object-rds.md) объекта метод [CreateObject](createobject-method-rds.md) , чтобы указать программы сервера по умолчанию, [RDSServer.DataFactory](datafactory-object-rdsserver.md)или собственную программу настраиваемый серверный (бизнес-объект). Программа сервера создается на сервере и ссылку на программу сервера или *прокси-сервера*, возвращается.

В этом руководстве использует программы сервера по умолчанию:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

