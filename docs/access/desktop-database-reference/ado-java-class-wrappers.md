---
title: Оболочки класса Java ADO
TOCTitle: ADO Java class wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 731e659f29d6fd504bab772867fb438985189e13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283319"
---
# <a name="ado-java-class-wrappers"></a>Оболочки класса Java ADO


**Область применения**: Access 2013, Office 2013

Этот код объявляет экземпляр оболочки класса ADO [Recordset](recordset-object-ado.md) и инициализирует его в одной строке кода. Кроме того, он объявляет переменные для каждого аргумента в методе [Open,](open-method-ado-recordset.md) особенно для [LockType](locktype-property-ado.md) и [CursorType](cursortype-property-ado.md) (так как Java не поддерживает нумерированные типы). Он открывает и закрывает объект **Recordset.** Установка для Rs1 NULL просто запланировать выпуск этой переменной, когда Java выполняет системный и периодический выпуск неиспользованных объектов.

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

