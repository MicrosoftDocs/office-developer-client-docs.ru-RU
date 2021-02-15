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
# <a name="ado-java-class-wrappers"></a><span data-ttu-id="26482-102">Оболочки класса Java ADO</span><span class="sxs-lookup"><span data-stu-id="26482-102">ADO Java class wrappers</span></span>


<span data-ttu-id="26482-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26482-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26482-104">Этот код объявляет экземпляр оболочки класса ADO [Recordset](recordset-object-ado.md) и инициализирует его в одной строке кода.</span><span class="sxs-lookup"><span data-stu-id="26482-104">This code declares an instance of the ADO [Recordset](recordset-object-ado.md) class wrapper and initializes it, all on the same line of code.</span></span> <span data-ttu-id="26482-105">Кроме того, он объявляет переменные для каждого аргумента в методе [Open,](open-method-ado-recordset.md) особенно для [LockType](locktype-property-ado.md) и [CursorType](cursortype-property-ado.md) (так как Java не поддерживает нумерированные типы).</span><span class="sxs-lookup"><span data-stu-id="26482-105">Further, it declares variables for each of the arguments in the [Open](open-method-ado-recordset.md) method, especially for [LockType](locktype-property-ado.md) and [CursorType](cursortype-property-ado.md) (because Java doesn't support enumerated types).</span></span> <span data-ttu-id="26482-106">Он открывает и закрывает объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="26482-106">It opens and closes the **Recordset** object.</span></span> <span data-ttu-id="26482-107">Установка для Rs1 NULL просто запланировать выпуск этой переменной, когда Java выполняет системный и периодический выпуск неиспользованных объектов.</span><span class="sxs-lookup"><span data-stu-id="26482-107">Setting Rs1 to NULL merely schedules that variable to be released when Java performs its systematic and intermittent release of unused objects.</span></span>

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

