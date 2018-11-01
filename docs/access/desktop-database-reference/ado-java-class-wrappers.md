---
title: Оболочки классов Java для ADO
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 602d3407d78843331fdb78ef728cebbc69bace14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889464"
---
# <a name="ado-java-class-wrappers"></a>Оболочки классов Java для ADO


**Применимо к**: Access 2013, Office 2013

Этот код объявляет экземпляр оболочки класс ADO [записей](recordset-object-ado.md) и инициализирует его, все в той же строке кода. Более того он объявляет переменные для каждого из аргументов в метод [Open](open-method-ado-recordset.md) особенно для [LockType для](locktype-property-ado.md) и [CursorType](cursortype-property-ado.md) (поскольку Java не поддерживает перечисляемые типы). Открывает и закрывает объект **набора записей** . Установка Rs1 NULL для просто планирует этой переменной нужно освободить при Java выполняет его систематического и временная выпуска неиспользуемых объектов.

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```

